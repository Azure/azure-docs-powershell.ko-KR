---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 8319a5bc0251e744ee898658b0a0a541f0ce86ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493926"
---
# <span data-ttu-id="65dcf-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="65dcf-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="65dcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="65dcf-103">컨테이너 서비스 에이전트 풀 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="65dcf-104">구문</span><span class="sxs-lookup"><span data-stu-id="65dcf-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65dcf-105">설명</span><span class="sxs-lookup"><span data-stu-id="65dcf-105">DESCRIPTION</span></span>
<span data-ttu-id="65dcf-106">**Add-AzContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스 에이전트 풀 프로필을 로컬 컨테이너 서비스 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="65dcf-107">예제</span><span class="sxs-lookup"><span data-stu-id="65dcf-107">EXAMPLES</span></span>

### <span data-ttu-id="65dcf-108">예제 1: 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="65dcf-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="65dcf-109">이 명령은 컨테이너 서비스 에이전트 풀 프로필을 로컬 컨테이너 서비스 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="65dcf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65dcf-110">PARAMETERS</span></span>

### <span data-ttu-id="65dcf-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="65dcf-111">-ContainerService</span></span>
<span data-ttu-id="65dcf-112">이 cmdlet이 에이전트 풀 프로필을 추가하는 컨테이너 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="65dcf-113">**ContainerService** 개체를 얻습니다. [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65dcf-114">-Count</span><span class="sxs-lookup"><span data-stu-id="65dcf-114">-Count</span></span>
<span data-ttu-id="65dcf-115">컨테이너를 호스트하는 에이전트 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="65dcf-116">이 매개 변수에 허용되는 값은 1에서 100까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="65dcf-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dcf-118">-DefaultProfile</span></span>
<span data-ttu-id="65dcf-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65dcf-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="65dcf-120">-DnsPrefix</span></span>
<span data-ttu-id="65dcf-121">이 cmdlet이 이 에이전트 풀에 대한 정식 도메인 이름을 만드는 데 사용하는 DNS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="65dcf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="65dcf-122">-Name</span></span>
<span data-ttu-id="65dcf-123">에이전트 풀 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="65dcf-124">이 값은 구독 및 리소스 그룹의 컨텍스트에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dcf-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="65dcf-125">-VmSize</span></span>
<span data-ttu-id="65dcf-126">에이전트에 대한 가상 머신의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dcf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65dcf-127">-Confirm</span></span>
<span data-ttu-id="65dcf-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65dcf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65dcf-129">-WhatIf</span></span>
<span data-ttu-id="65dcf-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="65dcf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65dcf-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65dcf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dcf-132">CommonParameters</span></span>
<span data-ttu-id="65dcf-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65dcf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dcf-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65dcf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dcf-135">입력</span><span class="sxs-lookup"><span data-stu-id="65dcf-135">INPUTS</span></span>

### <span data-ttu-id="65dcf-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="65dcf-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="65dcf-137">System.String</span><span class="sxs-lookup"><span data-stu-id="65dcf-137">System.String</span></span>

### <span data-ttu-id="65dcf-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="65dcf-138">System.Int32</span></span>

## <span data-ttu-id="65dcf-139">출력</span><span class="sxs-lookup"><span data-stu-id="65dcf-139">OUTPUTS</span></span>

### <span data-ttu-id="65dcf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="65dcf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="65dcf-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65dcf-141">NOTES</span></span>

## <span data-ttu-id="65dcf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65dcf-142">RELATED LINKS</span></span>

[<span data-ttu-id="65dcf-143">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="65dcf-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="65dcf-144">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="65dcf-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
