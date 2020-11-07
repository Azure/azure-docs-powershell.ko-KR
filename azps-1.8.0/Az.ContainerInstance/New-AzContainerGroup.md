---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 76719250ca7909d86d288b987b9598a58ab5fb88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701190"
---
# <span data-ttu-id="2e9b0-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2e9b0-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="2e9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e9b0-103">컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-103">Creates a container group.</span></span>

## <span data-ttu-id="2e9b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e9b0-104">SYNTAX</span></span>

### <span data-ttu-id="2e9b0-105">CreateContainerGroupBaseParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9b0-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="2e9b0-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9b0-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="2e9b0-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e9b0-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e9b0-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e9b0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2e9b0-109">DESCRIPTION</span></span>
<span data-ttu-id="2e9b0-110">**AzContainerGroup** cmdlet은 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="2e9b0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2e9b0-111">EXAMPLES</span></span>

### <span data-ttu-id="2e9b0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e9b0-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="2e9b0-113">이 명령은 최신 nginx image를 사용 하 여 컨테이너 그룹을 만들고 포트 8000 열기를 사용 하 여 공용 IP 주소를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="2e9b0-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="2e9b0-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="2e9b0-115">이 명령은 컨테이너 그룹을 만들고 컨테이너 내에서 사용자 지정 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="2e9b0-116">예제 3: 완성 된 실행 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="2e9b0-117">이 명령은 ' hello '를 출력 하는 컨테이너 그룹을 만들며 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="2e9b0-118">예제 4: Azure 컨테이너 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="2e9b0-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="2e9b0-119">이 명령은 Azure 컨테이너 레지스트리에서 nginx image를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="2e9b0-120">예제 5: 사용자 지정 컨테이너 이미지 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="2e9b0-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="2e9b0-121">이 명령은 사용자 지정 컨테이너 이미지 레지스트리의 사용자 지정 이미지를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="2e9b0-122">예제 6: Azure 파일 볼륨을 탑재 하는 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="2e9b0-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzFileVolumeShareName myshare -AzFileVolumeAccountKey $mycred -AzFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="2e9b0-123">이 명령은 제공 된 Azure 파일 공유를 탑재 하는 컨테이너 그룹을 만듭니다 `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="2e9b0-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="2e9b0-124">예제 7</span><span class="sxs-lookup"><span data-stu-id="2e9b0-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

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
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="2e9b0-125">이 명령은 최신 nginx image를 사용 하 여 시스템에 할당 된 id를 가진 컨테이너 그룹을 만들고 포트 8000를 열어 공용 IP 주소를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="2e9b0-126">예제 8</span><span class="sxs-lookup"><span data-stu-id="2e9b0-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

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
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="2e9b0-127">이 명령은 시스템을 할당 하 고 최신 nginx image를 사용 하 여 사용자 할당 id를 만들고 포트 8000을 열어 공용 IP 주소를 요청 하는 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="2e9b0-128">변수</span><span class="sxs-lookup"><span data-stu-id="2e9b0-128">PARAMETERS</span></span>

### <span data-ttu-id="2e9b0-129">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="2e9b0-129">-AssignIdentity</span></span>
<span data-ttu-id="2e9b0-130">시스템 할당 id 사용</span><span class="sxs-lookup"><span data-stu-id="2e9b0-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2e9b0-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="2e9b0-132">사용자 이름이 저장소 계정 이름이 고 키가 저장소 계정 키 인 경우 탑재할 Azure 파일 공유의 저장소 계정 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="2e9b0-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="2e9b0-134">Azure 파일 볼륨의 탑재 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="2e9b0-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="2e9b0-136">탑재할 Azure 파일 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-137">-명령</span><span class="sxs-lookup"><span data-stu-id="2e9b0-137">-Command</span></span>
<span data-ttu-id="2e9b0-138">컨테이너에서 실행할 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-138">The command to run in the container.</span></span>

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

### <span data-ttu-id="2e9b0-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="2e9b0-139">-Cpu</span></span>
<span data-ttu-id="2e9b0-140">필수 CPU 코어입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-140">The required CPU cores.</span></span>
<span data-ttu-id="2e9b0-141">기본값: 1</span><span class="sxs-lookup"><span data-stu-id="2e9b0-141">Default: 1</span></span>

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

### <span data-ttu-id="2e9b0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e9b0-142">-DefaultProfile</span></span>
<span data-ttu-id="2e9b0-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="2e9b0-144">-DnsNameLabel</span></span>
<span data-ttu-id="2e9b0-145">IP 주소의 DNS 이름 레이블</span><span class="sxs-lookup"><span data-stu-id="2e9b0-145">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="2e9b0-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="2e9b0-146">-EnvironmentVariable</span></span>
<span data-ttu-id="2e9b0-147">컨테이너 환경 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-147">The container environment variables.</span></span>

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

### <span data-ttu-id="2e9b0-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2e9b0-148">-IdentityId</span></span>
<span data-ttu-id="2e9b0-149">사용자가 할당 한 id Id</span><span class="sxs-lookup"><span data-stu-id="2e9b0-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2e9b0-150">-IdentityType</span></span>
<span data-ttu-id="2e9b0-151">관리 되는 id 형식</span><span class="sxs-lookup"><span data-stu-id="2e9b0-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e9b0-152">-이미지</span><span class="sxs-lookup"><span data-stu-id="2e9b0-152">-Image</span></span>
<span data-ttu-id="2e9b0-153">컨테이너 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-153">The container image.</span></span>

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

### <span data-ttu-id="2e9b0-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="2e9b0-154">-IpAddressType</span></span>
<span data-ttu-id="2e9b0-155">IP 주소 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-155">The IP address type.</span></span>

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

### <span data-ttu-id="2e9b0-156">-위치</span><span class="sxs-lookup"><span data-stu-id="2e9b0-156">-Location</span></span>
<span data-ttu-id="2e9b0-157">컨테이너 그룹 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-157">The container group Location.</span></span>
<span data-ttu-id="2e9b0-158">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-158">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="2e9b0-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="2e9b0-159">-MemoryInGB</span></span>
<span data-ttu-id="2e9b0-160">필요한 메모리 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-160">The required memory in GB.</span></span>
<span data-ttu-id="2e9b0-161">기본값: 1.5</span><span class="sxs-lookup"><span data-stu-id="2e9b0-161">Default: 1.5</span></span>

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

### <span data-ttu-id="2e9b0-162">-이름</span><span class="sxs-lookup"><span data-stu-id="2e9b0-162">-Name</span></span>
<span data-ttu-id="2e9b0-163">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-163">The container group name.</span></span>

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

### <span data-ttu-id="2e9b0-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="2e9b0-164">-OsType</span></span>
<span data-ttu-id="2e9b0-165">컨테이너 OS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-165">The container OS type.</span></span>
<span data-ttu-id="2e9b0-166">기본값: Linux</span><span class="sxs-lookup"><span data-stu-id="2e9b0-166">Default: Linux</span></span>

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

### <span data-ttu-id="2e9b0-167">-포트</span><span class="sxs-lookup"><span data-stu-id="2e9b0-167">-Port</span></span>
<span data-ttu-id="2e9b0-168">열리는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-168">The port(s) to open.</span></span> <span data-ttu-id="2e9b0-169">기본값: [80]</span><span class="sxs-lookup"><span data-stu-id="2e9b0-169">Default: [80]</span></span>

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

### <span data-ttu-id="2e9b0-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="2e9b0-170">-RegistryCredential</span></span>
<span data-ttu-id="2e9b0-171">사용자 지정 컨테이너 레지스트리 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-171">The custom container registry credential.</span></span>

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

### <span data-ttu-id="2e9b0-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="2e9b0-172">-RegistryServerDomain</span></span>
<span data-ttu-id="2e9b0-173">사용자 지정 컨테이너 레지스트리 로그인 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-173">The custom container registry login server.</span></span>

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

### <span data-ttu-id="2e9b0-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e9b0-174">-ResourceGroupName</span></span>
<span data-ttu-id="2e9b0-175">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-175">The resource group name.</span></span>

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

### <span data-ttu-id="2e9b0-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="2e9b0-176">-RestartPolicy</span></span>
<span data-ttu-id="2e9b0-177">컨테이너 다시 시작 정책.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-177">The container restart policy.</span></span> <span data-ttu-id="2e9b0-178">기본값: 항상</span><span class="sxs-lookup"><span data-stu-id="2e9b0-178">Default: Always</span></span>

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

### <span data-ttu-id="2e9b0-179">태그</span><span class="sxs-lookup"><span data-stu-id="2e9b0-179">-Tag</span></span>
<span data-ttu-id="2e9b0-180">{{채우기 태그 설명}}</span><span class="sxs-lookup"><span data-stu-id="2e9b0-180">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="2e9b0-181">-확인</span><span class="sxs-lookup"><span data-stu-id="2e9b0-181">-Confirm</span></span>
<span data-ttu-id="2e9b0-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e9b0-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e9b0-183">-WhatIf</span></span>
<span data-ttu-id="2e9b0-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e9b0-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e9b0-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e9b0-186">CommonParameters</span></span>
<span data-ttu-id="2e9b0-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e9b0-188">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e9b0-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e9b0-189">입력</span><span class="sxs-lookup"><span data-stu-id="2e9b0-189">INPUTS</span></span>

### <span data-ttu-id="2e9b0-190">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e9b0-190">System.String</span></span>

### <span data-ttu-id="2e9b0-191">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2e9b0-191">System.String[]</span></span>

### <span data-ttu-id="2e9b0-192">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2e9b0-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e9b0-193">출력</span><span class="sxs-lookup"><span data-stu-id="2e9b0-193">OUTPUTS</span></span>

### <span data-ttu-id="2e9b0-194">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2e9b0-195">상속자</span><span class="sxs-lookup"><span data-stu-id="2e9b0-195">NOTES</span></span>

## <span data-ttu-id="2e9b0-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e9b0-196">RELATED LINKS</span></span>
