---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537444"
---
# <span data-ttu-id="b0624-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b0624-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="b0624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0624-102">SYNOPSIS</span></span>
<span data-ttu-id="b0624-103">컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0624-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0624-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0624-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0624-105">DESCRIPTION</span></span>
<span data-ttu-id="b0624-106">**Add-AzureRmContainerServiceAgentPoolProfile** cmdlet은 로컬 컨테이너 서비스 개체에 컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="b0624-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0624-107">EXAMPLES</span></span>

### <span data-ttu-id="b0624-108">예제 1: 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="b0624-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="b0624-109">이 명령은 컨테이너 서비스 에이전트 풀 프로필을 로컬 컨테이너 서비스 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="b0624-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0624-110">PARAMETERS</span></span>

### <span data-ttu-id="b0624-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b0624-111">-ContainerService</span></span>
<span data-ttu-id="b0624-112">이 cmdlet이 에이전트 풀 프로필을 추가 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="b0624-113">**ContainerService** 개체를 얻으려면 [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="b0624-114">-카운트</span><span class="sxs-lookup"><span data-stu-id="b0624-114">-Count</span></span>
<span data-ttu-id="b0624-115">컨테이너를 호스트 하는 에이전트의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="b0624-116">이 매개 변수에 허용 되는 값은 1부터 100 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="b0624-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-117">The default value is 1.</span></span>

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

### <span data-ttu-id="b0624-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0624-118">-DefaultProfile</span></span>
<span data-ttu-id="b0624-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0624-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="b0624-120">-DnsPrefix</span></span>
<span data-ttu-id="b0624-121">이 cmdlet이이 에이전트 풀에 대해 정규화 된 도메인 이름을 만드는 데 사용 하는 DNS 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="b0624-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b0624-122">-Name</span></span>
<span data-ttu-id="b0624-123">에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="b0624-124">이 값은 구독 및 리소스 그룹의 컨텍스트에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="b0624-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="b0624-125">-VmSize</span></span>
<span data-ttu-id="b0624-126">에이전트에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="b0624-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b0624-127">-Confirm</span></span>
<span data-ttu-id="b0624-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0624-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0624-129">-WhatIf</span></span>
<span data-ttu-id="b0624-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0624-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0624-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0624-132">CommonParameters</span></span>
<span data-ttu-id="b0624-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0624-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0624-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0624-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0624-135">입력</span><span class="sxs-lookup"><span data-stu-id="b0624-135">INPUTS</span></span>

## <span data-ttu-id="b0624-136">출력</span><span class="sxs-lookup"><span data-stu-id="b0624-136">OUTPUTS</span></span>

## <span data-ttu-id="b0624-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b0624-137">NOTES</span></span>

## <span data-ttu-id="b0624-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0624-138">RELATED LINKS</span></span>

[<span data-ttu-id="b0624-139">새로운 AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="b0624-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="b0624-140">제거-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b0624-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
