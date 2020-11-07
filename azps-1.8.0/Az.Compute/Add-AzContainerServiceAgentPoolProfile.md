---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 4a356af4090fefe25956fb421b0df409e1edd79b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701385"
---
# <span data-ttu-id="eb914-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="eb914-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="eb914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb914-102">SYNOPSIS</span></span>
<span data-ttu-id="eb914-103">컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="eb914-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb914-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb914-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb914-105">DESCRIPTION</span></span>
<span data-ttu-id="eb914-106">**Add-AzContainerServiceAgentPoolProfile** cmdlet은 로컬 컨테이너 서비스 개체에 컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="eb914-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eb914-107">EXAMPLES</span></span>

### <span data-ttu-id="eb914-108">예제 1: 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="eb914-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="eb914-109">이 명령은 컨테이너 서비스 에이전트 풀 프로필을 로컬 컨테이너 서비스 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="eb914-110">변수</span><span class="sxs-lookup"><span data-stu-id="eb914-110">PARAMETERS</span></span>

### <span data-ttu-id="eb914-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="eb914-111">-ContainerService</span></span>
<span data-ttu-id="eb914-112">이 cmdlet이 에이전트 풀 프로필을 추가 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="eb914-113">**ContainerService** 개체를 얻으려면 [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="eb914-114">-카운트</span><span class="sxs-lookup"><span data-stu-id="eb914-114">-Count</span></span>
<span data-ttu-id="eb914-115">컨테이너를 호스트 하는 에이전트의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="eb914-116">이 매개 변수에 허용 되는 값은 1부터 100 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="eb914-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-117">The default value is 1.</span></span>

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

### <span data-ttu-id="eb914-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb914-118">-DefaultProfile</span></span>
<span data-ttu-id="eb914-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb914-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="eb914-120">-DnsPrefix</span></span>
<span data-ttu-id="eb914-121">이 cmdlet이이 에이전트 풀에 대해 정규화 된 도메인 이름을 만드는 데 사용 하는 DNS 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="eb914-122">-이름</span><span class="sxs-lookup"><span data-stu-id="eb914-122">-Name</span></span>
<span data-ttu-id="eb914-123">에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="eb914-124">이 값은 구독 및 리소스 그룹의 컨텍스트에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="eb914-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="eb914-125">-VmSize</span></span>
<span data-ttu-id="eb914-126">에이전트에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="eb914-127">-확인</span><span class="sxs-lookup"><span data-stu-id="eb914-127">-Confirm</span></span>
<span data-ttu-id="eb914-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb914-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb914-129">-WhatIf</span></span>
<span data-ttu-id="eb914-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb914-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb914-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb914-132">CommonParameters</span></span>
<span data-ttu-id="eb914-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb914-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb914-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb914-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb914-135">입력</span><span class="sxs-lookup"><span data-stu-id="eb914-135">INPUTS</span></span>

### <span data-ttu-id="eb914-136">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="eb914-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="eb914-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb914-137">System.String</span></span>

### <span data-ttu-id="eb914-138">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="eb914-138">System.Int32</span></span>

## <span data-ttu-id="eb914-139">출력</span><span class="sxs-lookup"><span data-stu-id="eb914-139">OUTPUTS</span></span>

### <span data-ttu-id="eb914-140">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="eb914-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="eb914-141">상속자</span><span class="sxs-lookup"><span data-stu-id="eb914-141">NOTES</span></span>

## <span data-ttu-id="eb914-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb914-142">RELATED LINKS</span></span>

[<span data-ttu-id="eb914-143">새로운 AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="eb914-143">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="eb914-144">제거-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="eb914-144">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
