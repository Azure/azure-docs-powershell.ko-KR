---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702837"
---
# <span data-ttu-id="6d796-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="6d796-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="6d796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d796-102">SYNOPSIS</span></span>
<span data-ttu-id="6d796-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d796-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d796-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d796-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d796-105">DESCRIPTION</span></span>
<span data-ttu-id="6d796-106">**AzureRmServiceBusNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="6d796-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d796-107">EXAMPLES</span></span>

### <span data-ttu-id="6d796-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d796-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="6d796-109">지정 된 리소스 그룹에서 서비스 버스 네임 스페이스를 제거 `SB-Example1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="6d796-110">변수</span><span class="sxs-lookup"><span data-stu-id="6d796-110">PARAMETERS</span></span>

### <span data-ttu-id="6d796-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d796-111">-DefaultProfile</span></span>
<span data-ttu-id="6d796-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d796-113">-이름</span><span class="sxs-lookup"><span data-stu-id="6d796-113">-Name</span></span>
<span data-ttu-id="6d796-114">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-114">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d796-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d796-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d796-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d796-117">-확인</span><span class="sxs-lookup"><span data-stu-id="6d796-117">-Confirm</span></span>
<span data-ttu-id="6d796-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d796-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d796-119">-WhatIf</span></span>
<span data-ttu-id="6d796-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d796-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d796-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d796-122">CommonParameters</span></span>
<span data-ttu-id="6d796-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d796-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d796-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d796-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d796-125">입력</span><span class="sxs-lookup"><span data-stu-id="6d796-125">INPUTS</span></span>

### <span data-ttu-id="6d796-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d796-126">-ResourceGroup</span></span>
 <span data-ttu-id="6d796-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d796-127">System.String</span></span>

### <span data-ttu-id="6d796-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6d796-128">-NamespaceName</span></span>
 <span data-ttu-id="6d796-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d796-129">System.String</span></span>

## <span data-ttu-id="6d796-130">출력</span><span class="sxs-lookup"><span data-stu-id="6d796-130">OUTPUTS</span></span>

### <span data-ttu-id="6d796-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="6d796-131">System.Object</span></span>

## <span data-ttu-id="6d796-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6d796-132">NOTES</span></span>

## <span data-ttu-id="6d796-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d796-133">RELATED LINKS</span></span>

