---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531764"
---
# <span data-ttu-id="64d18-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="64d18-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="64d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d18-102">SYNOPSIS</span></span>
<span data-ttu-id="64d18-103">컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64d18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64d18-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64d18-105">DESCRIPTION</span></span>
<span data-ttu-id="64d18-106">**Add-AzureRmContainerServiceAgentPoolProfile** cmdlet은 로컬 컨테이너 서비스 개체에 컨테이너 서비스 에이전트 풀 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="64d18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="64d18-107">EXAMPLES</span></span>

### <span data-ttu-id="64d18-108">예제 1: 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="64d18-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="64d18-109">이 명령은 컨테이너 서비스 에이전트 풀 프로필을 로컬 컨테이너 서비스 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="64d18-110">변수</span><span class="sxs-lookup"><span data-stu-id="64d18-110">PARAMETERS</span></span>

### <span data-ttu-id="64d18-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="64d18-111">-ContainerService</span></span>
<span data-ttu-id="64d18-112">이 cmdlet이 에이전트 풀 프로필을 추가 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="64d18-113">**ContainerService** 개체를 얻으려면 [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-114">-카운트</span><span class="sxs-lookup"><span data-stu-id="64d18-114">-Count</span></span>
<span data-ttu-id="64d18-115">컨테이너를 호스트 하는 에이전트의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="64d18-116">이 매개 변수에 허용 되는 값은 1부터 100 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="64d18-117">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="64d18-118">-DnsPrefix</span></span>
<span data-ttu-id="64d18-119">이 cmdlet이이 에이전트 풀에 대해 정규화 된 도메인 이름을 만드는 데 사용 하는 DNS 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-120">-이름</span><span class="sxs-lookup"><span data-stu-id="64d18-120">-Name</span></span>
<span data-ttu-id="64d18-121">에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="64d18-122">이 값은 구독 및 리소스 그룹의 컨텍스트에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-122">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="64d18-123">-VmSize</span></span>
<span data-ttu-id="64d18-124">에이전트에 대 한 가상 컴퓨터의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-124">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-125">-확인</span><span class="sxs-lookup"><span data-stu-id="64d18-125">-Confirm</span></span>
<span data-ttu-id="64d18-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d18-127">-WhatIf</span></span>
<span data-ttu-id="64d18-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64d18-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d18-130">CommonParameters</span></span>
<span data-ttu-id="64d18-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d18-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d18-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d18-133">입력</span><span class="sxs-lookup"><span data-stu-id="64d18-133">INPUTS</span></span>

### <span data-ttu-id="64d18-134">않아야</span><span class="sxs-lookup"><span data-stu-id="64d18-134">None</span></span>
<span data-ttu-id="64d18-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64d18-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64d18-136">출력</span><span class="sxs-lookup"><span data-stu-id="64d18-136">OUTPUTS</span></span>

## <span data-ttu-id="64d18-137">상속자</span><span class="sxs-lookup"><span data-stu-id="64d18-137">NOTES</span></span>

## <span data-ttu-id="64d18-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64d18-138">RELATED LINKS</span></span>

[<span data-ttu-id="64d18-139">새로운 AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="64d18-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="64d18-140">제거-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="64d18-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
