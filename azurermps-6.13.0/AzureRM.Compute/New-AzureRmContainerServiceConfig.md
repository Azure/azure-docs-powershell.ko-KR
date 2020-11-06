---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532087"
---
# <span data-ttu-id="0508e-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="0508e-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="0508e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0508e-102">SYNOPSIS</span></span>
<span data-ttu-id="0508e-103">컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0508e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0508e-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0508e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0508e-105">DESCRIPTION</span></span>
<span data-ttu-id="0508e-106">**AzureRmContainerServiceConfig** cmdlet은 컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="0508e-107">이 개체를 New-AzureRmContainerService cmdlet에 제공 하 여 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="0508e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0508e-108">EXAMPLES</span></span>

### <span data-ttu-id="0508e-109">예제 1: 컨테이너 서비스 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="0508e-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="0508e-110">이 명령은 컨테이너를 만든 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="0508e-111">명령은 컨테이너 서비스 구성에 대 한 다양 한 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="0508e-112">이 명령은 파이프라인 연산자를 사용 하 여 Add-AzureRmContainerServiceAgentPoolProfile cmdlet에 구성 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="0508e-113">해당 cmdlet은 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="0508e-114">**New-AzureRmContainerService** 의 *ContainerService* 매개 변수에 대해 $Container에서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="0508e-115">변수</span><span class="sxs-lookup"><span data-stu-id="0508e-115">PARAMETERS</span></span>

### <span data-ttu-id="0508e-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="0508e-116">-AdminUsername</span></span>
<span data-ttu-id="0508e-117">Linux 기반 컨테이너 서비스에 사용할 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="0508e-118">-AgentPoolProfile</span></span>
<span data-ttu-id="0508e-119">컨테이너 서비스에 대 한 에이전트 풀 프로필 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="0508e-120">Add-AzureRmContainerServiceAgentPoolProfile cmdlet을 사용 하 여 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="0508e-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="0508e-122">사용자 지정 프로필 orchestrator를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0508e-123">-DefaultProfile</span></span>
<span data-ttu-id="0508e-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0508e-125">-위치</span><span class="sxs-lookup"><span data-stu-id="0508e-125">-Location</span></span>
<span data-ttu-id="0508e-126">컨테이너 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="0508e-127">-MasterCount</span></span>
<span data-ttu-id="0508e-128">만들 마스터 가상 컴퓨터 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="0508e-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="0508e-130">마스터 가상 컴퓨터에 대 한 DNS 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="0508e-131">-OrchestratorType</span></span>
<span data-ttu-id="0508e-132">컨테이너 서비스에 대 한 orchestrator 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="0508e-133">이 매개 변수에 허용 되는 값은 DCOS 및 Swarm입니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="0508e-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="0508e-135">주 프로필 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="0508e-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="0508e-137">주 프로필 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0508e-138">-SshPublicKey</span></span>
<span data-ttu-id="0508e-139">Linux 기반 컨테이너 서비스에 대 한 SSH 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-140">태그</span><span class="sxs-lookup"><span data-stu-id="0508e-140">-Tag</span></span>
<span data-ttu-id="0508e-141">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0508e-142">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0508e-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="0508e-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="0508e-144">이 구성으로 컨테이너 서비스 가상 컴퓨터에 대 한 진단을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="0508e-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="0508e-146">Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="0508e-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="0508e-148">Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0508e-149">-확인</span><span class="sxs-lookup"><span data-stu-id="0508e-149">-Confirm</span></span>
<span data-ttu-id="0508e-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0508e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0508e-151">-WhatIf</span></span>
<span data-ttu-id="0508e-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0508e-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0508e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0508e-154">CommonParameters</span></span>
<span data-ttu-id="0508e-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0508e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0508e-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0508e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0508e-157">입력</span><span class="sxs-lookup"><span data-stu-id="0508e-157">INPUTS</span></span>

### <span data-ttu-id="0508e-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0508e-158">System.String</span></span>

### <span data-ttu-id="0508e-159">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0508e-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0508e-160">시스템 Null 허용 ' 1 [[ContainerServiceOrchestratorTypes, Microsoft azure. 21.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0508e-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0508e-161">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="0508e-161">System.Int32</span></span>

### <span data-ttu-id="0508e-162">Microsoft ContainerServiceAgentPoolProfile []을 (를)</span><span class="sxs-lookup"><span data-stu-id="0508e-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="0508e-163">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="0508e-163">System.String[]</span></span>

### <span data-ttu-id="0508e-164">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0508e-164">System.Boolean</span></span>

## <span data-ttu-id="0508e-165">출력</span><span class="sxs-lookup"><span data-stu-id="0508e-165">OUTPUTS</span></span>

### <span data-ttu-id="0508e-166">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="0508e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0508e-167">상속자</span><span class="sxs-lookup"><span data-stu-id="0508e-167">NOTES</span></span>

## <span data-ttu-id="0508e-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0508e-168">RELATED LINKS</span></span>

[<span data-ttu-id="0508e-169">추가-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="0508e-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="0508e-170">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="0508e-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
