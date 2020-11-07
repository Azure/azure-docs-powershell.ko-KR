---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 5631ab93c4c9d0fd89b56043d32bc685b042ace9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697389"
---
# <span data-ttu-id="d01bd-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d01bd-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="d01bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d01bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d01bd-103">컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="d01bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d01bd-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d01bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d01bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d01bd-106">**AzContainerServiceConfig** cmdlet은 컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="d01bd-107">이 개체를 New-AzContainerService cmdlet에 제공 하 여 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="d01bd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d01bd-108">EXAMPLES</span></span>

### <span data-ttu-id="d01bd-109">예제 1: 컨테이너 서비스 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="d01bd-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="d01bd-110">이 명령은 컨테이너를 만든 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="d01bd-111">명령은 컨테이너 서비스 구성에 대 한 다양 한 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="d01bd-112">이 명령은 파이프라인 연산자를 사용 하 여 Add-AzContainerServiceAgentPoolProfile cmdlet에 구성 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="d01bd-113">해당 cmdlet은 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="d01bd-114">**New-AzContainerService** 의 *ContainerService* 매개 변수에 대해 $Container에서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="d01bd-115">변수</span><span class="sxs-lookup"><span data-stu-id="d01bd-115">PARAMETERS</span></span>

### <span data-ttu-id="d01bd-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d01bd-116">-AdminUsername</span></span>
<span data-ttu-id="d01bd-117">Linux 기반 컨테이너 서비스에 사용할 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d01bd-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d01bd-118">-AgentPoolProfile</span></span>
<span data-ttu-id="d01bd-119">컨테이너 서비스에 대 한 에이전트 풀 프로필 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="d01bd-120">Add-AzContainerServiceAgentPoolProfile cmdlet을 사용 하 여 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="d01bd-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="d01bd-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="d01bd-122">사용자 지정 프로필 orchestrator를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="d01bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01bd-123">-DefaultProfile</span></span>
<span data-ttu-id="d01bd-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d01bd-125">-위치</span><span class="sxs-lookup"><span data-stu-id="d01bd-125">-Location</span></span>
<span data-ttu-id="d01bd-126">컨테이너 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="d01bd-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d01bd-127">-MasterCount</span></span>
<span data-ttu-id="d01bd-128">만들 마스터 가상 컴퓨터 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="d01bd-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="d01bd-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="d01bd-130">마스터 가상 컴퓨터에 대 한 DNS 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="d01bd-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="d01bd-131">-OrchestratorType</span></span>
<span data-ttu-id="d01bd-132">컨테이너 서비스에 대 한 orchestrator 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="d01bd-133">이 매개 변수에 허용 되는 값은 DCOS 및 Swarm입니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="d01bd-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="d01bd-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="d01bd-135">주 프로필 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="d01bd-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="d01bd-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="d01bd-137">주 프로필 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="d01bd-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d01bd-138">-SshPublicKey</span></span>
<span data-ttu-id="d01bd-139">Linux 기반 컨테이너 서비스에 대 한 SSH 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d01bd-140">태그</span><span class="sxs-lookup"><span data-stu-id="d01bd-140">-Tag</span></span>
<span data-ttu-id="d01bd-141">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d01bd-142">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d01bd-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d01bd-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d01bd-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="d01bd-144">이 구성으로 컨테이너 서비스 가상 컴퓨터에 대 한 진단을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="d01bd-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="d01bd-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="d01bd-146">Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d01bd-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="d01bd-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="d01bd-148">Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d01bd-149">-확인</span><span class="sxs-lookup"><span data-stu-id="d01bd-149">-Confirm</span></span>
<span data-ttu-id="d01bd-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01bd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d01bd-151">-WhatIf</span></span>
<span data-ttu-id="d01bd-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d01bd-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01bd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01bd-154">CommonParameters</span></span>
<span data-ttu-id="d01bd-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d01bd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01bd-156">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d01bd-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01bd-157">입력</span><span class="sxs-lookup"><span data-stu-id="d01bd-157">INPUTS</span></span>

### <span data-ttu-id="d01bd-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d01bd-158">System.String</span></span>

### <span data-ttu-id="d01bd-159">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d01bd-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d01bd-160">시스템 Null 허용 ' 1 [[ContainerServiceOrchestratorTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d01bd-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d01bd-161">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="d01bd-161">System.Int32</span></span>

### <span data-ttu-id="d01bd-162">Microsoft ContainerServiceAgentPoolProfile []을 (를)</span><span class="sxs-lookup"><span data-stu-id="d01bd-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="d01bd-163">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="d01bd-163">System.String[]</span></span>

### <span data-ttu-id="d01bd-164">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d01bd-164">System.Boolean</span></span>

## <span data-ttu-id="d01bd-165">출력</span><span class="sxs-lookup"><span data-stu-id="d01bd-165">OUTPUTS</span></span>

### <span data-ttu-id="d01bd-166">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="d01bd-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d01bd-167">상속자</span><span class="sxs-lookup"><span data-stu-id="d01bd-167">NOTES</span></span>

## <span data-ttu-id="d01bd-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d01bd-168">RELATED LINKS</span></span>

[<span data-ttu-id="d01bd-169">추가-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d01bd-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d01bd-170">새로운 AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d01bd-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
