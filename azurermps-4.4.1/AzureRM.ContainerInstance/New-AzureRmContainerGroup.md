---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534152"
---
# <span data-ttu-id="a7088-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a7088-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="a7088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7088-102">SYNOPSIS</span></span>
<span data-ttu-id="a7088-103">컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7088-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7088-104">SYNTAX</span></span>

### <span data-ttu-id="a7088-105">CreateContainerGroupBaseParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7088-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7088-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="a7088-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7088-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a7088-107">DESCRIPTION</span></span>
<span data-ttu-id="a7088-108">**AzureRmContainerGroup** cmdlet은 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="a7088-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a7088-109">EXAMPLES</span></span>

### <span data-ttu-id="a7088-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7088-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="a7088-111">이 명령은 최신 nginx image를 사용 하 여 컨테이너 그룹을 만들고 포트 8000 열기를 사용 하 여 공용 IP 주소를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="a7088-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a7088-112">Example 2</span></span>
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
```

<span data-ttu-id="a7088-113">이 명령은 컨테이너 그룹을 만들고 컨테이너 내에서 사용자 지정 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="a7088-114">예제 3: Azure 컨테이너 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a7088-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="a7088-115">이 명령은 Azure 컨테이너 레지스트리에서 nginx image를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="a7088-116">예제 4: 사용자 지정 컨테이너 이미지 레지스트리의 이미지를 사용 하 여 컨테이너 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a7088-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="a7088-117">이 명령은 사용자 지정 컨테이너 이미지 레지스트리의 사용자 지정 이미지를 사용 하 여 컨테이너 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="a7088-118">변수</span><span class="sxs-lookup"><span data-stu-id="a7088-118">PARAMETERS</span></span>

### <span data-ttu-id="a7088-119">-명령</span><span class="sxs-lookup"><span data-stu-id="a7088-119">-Command</span></span>
<span data-ttu-id="a7088-120">컨테이너에서 실행할 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="a7088-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a7088-121">-Confirm</span></span>
<span data-ttu-id="a7088-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7088-123">-Cpu</span><span class="sxs-lookup"><span data-stu-id="a7088-123">-Cpu</span></span>
<span data-ttu-id="a7088-124">필수 CPU 코어입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-124">The required CPU cores.</span></span>
<span data-ttu-id="a7088-125">기본값: 1</span><span class="sxs-lookup"><span data-stu-id="a7088-125">Default: 1</span></span>

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

### <span data-ttu-id="a7088-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="a7088-126">-EnvironmentVariable</span></span>
<span data-ttu-id="a7088-127">컨테이너 환경 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-127">The container environment variables.</span></span>

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

### <span data-ttu-id="a7088-128">-이미지</span><span class="sxs-lookup"><span data-stu-id="a7088-128">-Image</span></span>
<span data-ttu-id="a7088-129">컨테이너 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7088-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="a7088-130">-IpAddressType</span></span>
<span data-ttu-id="a7088-131">IP 주소 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-131">The IP address type.</span></span>

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

### <span data-ttu-id="a7088-132">-위치</span><span class="sxs-lookup"><span data-stu-id="a7088-132">-Location</span></span>
<span data-ttu-id="a7088-133">컨테이너 그룹 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-133">The container group Location.</span></span>
<span data-ttu-id="a7088-134">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="a7088-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="a7088-135">-MemoryInGB</span></span>
<span data-ttu-id="a7088-136">필요한 메모리 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-136">The required memory in GB.</span></span>
<span data-ttu-id="a7088-137">기본값: 1.5</span><span class="sxs-lookup"><span data-stu-id="a7088-137">Default: 1.5</span></span>

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

### <span data-ttu-id="a7088-138">-이름</span><span class="sxs-lookup"><span data-stu-id="a7088-138">-Name</span></span>
<span data-ttu-id="a7088-139">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-139">The container group name.</span></span>

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

### <span data-ttu-id="a7088-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="a7088-140">-OsType</span></span>
<span data-ttu-id="a7088-141">컨테이너 OS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-141">The container OS type.</span></span>
<span data-ttu-id="a7088-142">기본값: Linux</span><span class="sxs-lookup"><span data-stu-id="a7088-142">Default: Linux</span></span>

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

### <span data-ttu-id="a7088-143">-포트</span><span class="sxs-lookup"><span data-stu-id="a7088-143">-Port</span></span>
<span data-ttu-id="a7088-144">열려는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-144">The port to open.</span></span>
<span data-ttu-id="a7088-145">기본값: 80</span><span class="sxs-lookup"><span data-stu-id="a7088-145">Default: 80</span></span>

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

### <span data-ttu-id="a7088-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a7088-146">-RegistryCredential</span></span>
<span data-ttu-id="a7088-147">사용자 지정 컨테이너 레지스트리 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7088-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="a7088-148">-RegistryServerDomain</span></span>
<span data-ttu-id="a7088-149">사용자 지정 컨테이너 레지스트리 로그인 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7088-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7088-150">-ResourceGroupName</span></span>
<span data-ttu-id="a7088-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-151">The resource group name.</span></span>

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

### <span data-ttu-id="a7088-152">태그</span><span class="sxs-lookup"><span data-stu-id="a7088-152">-Tag</span></span>
<span data-ttu-id="a7088-153">{{채우기 태그 설명}}</span><span class="sxs-lookup"><span data-stu-id="a7088-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="a7088-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7088-154">-WhatIf</span></span>
<span data-ttu-id="a7088-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7088-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7088-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7088-157">-DefaultProfile</span></span>
<span data-ttu-id="a7088-158">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7088-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7088-159">CommonParameters</span></span>
<span data-ttu-id="a7088-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7088-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7088-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7088-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7088-162">입력</span><span class="sxs-lookup"><span data-stu-id="a7088-162">INPUTS</span></span>

### <span data-ttu-id="a7088-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7088-163">System.String</span></span>
<span data-ttu-id="a7088-164">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a7088-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a7088-165">출력</span><span class="sxs-lookup"><span data-stu-id="a7088-165">OUTPUTS</span></span>

### <span data-ttu-id="a7088-166">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="a7088-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a7088-167">상속자</span><span class="sxs-lookup"><span data-stu-id="a7088-167">NOTES</span></span>

## <span data-ttu-id="a7088-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7088-168">RELATED LINKS</span></span>

