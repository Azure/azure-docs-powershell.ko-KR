---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530217"
---
# <span data-ttu-id="a4107-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4107-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="a4107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4107-102">SYNOPSIS</span></span>
<span data-ttu-id="a4107-103">Get-AzureRmInterfaceEndpoint cmdlet은 인터페이스 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4107-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4107-104">SYNTAX</span></span>

### <span data-ttu-id="a4107-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4107-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4107-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4107-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4107-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a4107-107">DESCRIPTION</span></span>
<span data-ttu-id="a4107-108">**Get-AzureRmInterfaceEndpoint** Cmdlet은 인터페이스 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="a4107-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a4107-109">EXAMPLES</span></span>

### <span data-ttu-id="a4107-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4107-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4107-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 InterfaceEndpoint1 이라는 인터페이스 끝점을 가져와이를 $interfaceendpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="a4107-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a4107-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="a4107-113">이 명령은 resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 인 인터페이스 끝점을 가져와이를 $interfaceendpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="a4107-114">변수</span><span class="sxs-lookup"><span data-stu-id="a4107-114">PARAMETERS</span></span>

### <span data-ttu-id="a4107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4107-115">-DefaultProfile</span></span>
<span data-ttu-id="a4107-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4107-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a4107-117">-Name</span></span>
<span data-ttu-id="a4107-118">인터페이스 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4107-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4107-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4107-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4107-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4107-121">-ResourceId</span></span>
<span data-ttu-id="a4107-122">{{ResourceId: 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="a4107-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4107-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a4107-123">-Confirm</span></span>
<span data-ttu-id="a4107-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4107-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4107-125">-WhatIf</span></span>
<span data-ttu-id="a4107-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4107-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4107-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4107-128">CommonParameters</span></span>
<span data-ttu-id="a4107-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4107-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a4107-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4107-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4107-131">입력</span><span class="sxs-lookup"><span data-stu-id="a4107-131">INPUTS</span></span>

### <span data-ttu-id="a4107-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a4107-132">System.String</span></span>


## <span data-ttu-id="a4107-133">출력</span><span class="sxs-lookup"><span data-stu-id="a4107-133">OUTPUTS</span></span>

### <span data-ttu-id="a4107-134">Microsoft. 네트워크 모델. Ps인터페이스 끝점</span><span class="sxs-lookup"><span data-stu-id="a4107-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="a4107-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a4107-135">NOTES</span></span>

## <span data-ttu-id="a4107-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4107-136">RELATED LINKS</span></span>
