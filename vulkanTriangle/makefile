CFLAGS = -std=c++17 -O2
LDFLAGS = -lglfw -lvulkan -ldl -lpthread -lX11 -lXxf86vm -lXrandr -lXi

VulkanTriangle: main.cpp
	g++ $(CFLAGS) -o VulkanTriangle main.cpp $(LDFLAGS)
	glslangValidator -V shaders/shader.frag -o shaders/frag.spv
	glslangValidator -V shaders/shader.vert -o shaders/vert.spv

.PHONY: test clean

test: VulkanTriangle
	./VulkanTriangle

clean:
	rm -f VulkanTriangle shaders/*.spv
