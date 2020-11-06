---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526220"
---
# <span data-ttu-id="41474-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="41474-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="41474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41474-102">SYNOPSIS</span></span>
<span data-ttu-id="41474-103">컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41474-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41474-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41474-104">SYNTAX</span></span>

### <span data-ttu-id="41474-105">CreateContainerGroupBaseParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="41474-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41474-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="41474-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41474-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41474-107">DESCRIPTION</span></span>
<span data-ttu-id="41474-108">**AzureRmContainerGroup** cmdlet은 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41474-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="41474-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41474-109">EXAMPLES</span></span>

### <span data-ttu-id="41474-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="41474-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-111">이 명령은 최신 nginx image를 사용 하 여 컨테이너 그룹을 만들고 포트 8000 열기를 사용 하 여 공용 IP 주소를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="41474-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="41474-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="41474-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-113">이 명령은 컨테이너 그룹을 만들고 컨테이너 내에서 사용자 지정 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="41474-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="41474-114">예제 3: 완성 된 실행 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41474-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-115">이 명령은 ' hello '를 출력 하는 컨테이너 그룹을 만들며 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41474-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="41474-116">예제 4: Azure 컨테이너 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="41474-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-117">이 명령은 Azure 컨테이너 레지스트리에서 nginx image를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41474-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="41474-118">예제 5: 사용자 지정 컨테이너 이미지 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="41474-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-119">이 명령은 사용자 지정 컨테이너 이미지 레지스트리의 사용자 지정 이미지를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41474-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="41474-120">예제 6: Azure 파일 볼륨을 탑재 하는 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="41474-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="41474-121">이 명령은 제공 된 Azure 파일 공유를 탑재 하는 컨테이너 그룹을 만듭니다 `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="41474-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="41474-122">변수</span><span class="sxs-lookup"><span data-stu-id="41474-122">PARAMETERS</span></span>

### <span data-ttu-id="41474-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="41474-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="41474-124">사용자 이름이 저장소 계정 이름이 고 키가 저장소 계정 키 인 경우 탑재할 Azure 파일 공유의 저장소 계정 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="41474-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="41474-126">Azure 파일 볼륨의 탑재 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="41474-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="41474-128">탑재할 Azure 파일 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-129">-명령</span><span class="sxs-lookup"><span data-stu-id="41474-129">-Command</span></span>
<span data-ttu-id="41474-130">컨테이너에서 실행할 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-130">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-131">-Cpu</span><span class="sxs-lookup"><span data-stu-id="41474-131">-Cpu</span></span>
<span data-ttu-id="41474-132">필수 CPU 코어입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-132">The required CPU cores.</span></span>
<span data-ttu-id="41474-133">기본값: 1</span><span class="sxs-lookup"><span data-stu-id="41474-133">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41474-134">-DefaultProfile</span></span>
<span data-ttu-id="41474-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="41474-136">-DnsNameLabel</span></span>
<span data-ttu-id="41474-137">IP 주소의 DNS 이름 레이블</span><span class="sxs-lookup"><span data-stu-id="41474-137">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="41474-138">-EnvironmentVariable</span></span>
<span data-ttu-id="41474-139">컨테이너 환경 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-139">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-140">-이미지</span><span class="sxs-lookup"><span data-stu-id="41474-140">-Image</span></span>
<span data-ttu-id="41474-141">컨테이너 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-141">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="41474-142">-IpAddressType</span></span>
<span data-ttu-id="41474-143">IP 주소 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-143">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-144">-위치</span><span class="sxs-lookup"><span data-stu-id="41474-144">-Location</span></span>
<span data-ttu-id="41474-145">컨테이너 그룹 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-145">The container group Location.</span></span>
<span data-ttu-id="41474-146">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="41474-146">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="41474-147">-MemoryInGB</span></span>
<span data-ttu-id="41474-148">필요한 메모리 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-148">The required memory in GB.</span></span>
<span data-ttu-id="41474-149">기본값: 1.5</span><span class="sxs-lookup"><span data-stu-id="41474-149">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-150">-이름</span><span class="sxs-lookup"><span data-stu-id="41474-150">-Name</span></span>
<span data-ttu-id="41474-151">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-151">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41474-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="41474-152">-OsType</span></span>
<span data-ttu-id="41474-153">컨테이너 OS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-153">The container OS type.</span></span>
<span data-ttu-id="41474-154">기본값: Linux</span><span class="sxs-lookup"><span data-stu-id="41474-154">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-155">-포트</span><span class="sxs-lookup"><span data-stu-id="41474-155">-Port</span></span>
<span data-ttu-id="41474-156">열리는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-156">The port(s) to open.</span></span> <span data-ttu-id="41474-157">기본값: [80]</span><span class="sxs-lookup"><span data-stu-id="41474-157">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="41474-158">-RegistryCredential</span></span>
<span data-ttu-id="41474-159">사용자 지정 컨테이너 레지스트리 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-159">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="41474-160">-RegistryServerDomain</span></span>
<span data-ttu-id="41474-161">사용자 지정 컨테이너 레지스트리 로그인 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-161">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41474-162">-ResourceGroupName</span></span>
<span data-ttu-id="41474-163">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41474-163">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41474-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="41474-164">-RestartPolicy</span></span>
<span data-ttu-id="41474-165">컨테이너 다시 시작 정책.</span><span class="sxs-lookup"><span data-stu-id="41474-165">The container restart policy.</span></span> <span data-ttu-id="41474-166">기본값: 항상</span><span class="sxs-lookup"><span data-stu-id="41474-166">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-167">태그</span><span class="sxs-lookup"><span data-stu-id="41474-167">-Tag</span></span>
<span data-ttu-id="41474-168">{{채우기 태그 설명}}</span><span class="sxs-lookup"><span data-stu-id="41474-168">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41474-169">-확인</span><span class="sxs-lookup"><span data-stu-id="41474-169">-Confirm</span></span>
<span data-ttu-id="41474-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41474-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41474-171">-WhatIf</span></span>
<span data-ttu-id="41474-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41474-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41474-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41474-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41474-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41474-174">CommonParameters</span></span>
<span data-ttu-id="41474-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41474-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41474-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41474-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41474-177">입력</span><span class="sxs-lookup"><span data-stu-id="41474-177">INPUTS</span></span>

### <span data-ttu-id="41474-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41474-178">System.String</span></span>

### <span data-ttu-id="41474-179">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="41474-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41474-180">출력</span><span class="sxs-lookup"><span data-stu-id="41474-180">OUTPUTS</span></span>

### <span data-ttu-id="41474-181">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="41474-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="41474-182">상속자</span><span class="sxs-lookup"><span data-stu-id="41474-182">NOTES</span></span>

## <span data-ttu-id="41474-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41474-183">RELATED LINKS</span></span>
