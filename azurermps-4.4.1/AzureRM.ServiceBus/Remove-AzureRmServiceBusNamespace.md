---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529146"
---
# <span data-ttu-id="d0a35-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d0a35-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="d0a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a35-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a35-103">지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0a35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0a35-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a35-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0a35-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a35-106">**AzureRmServiceBusNamespace** cmdlet은 지정 된 리소스 그룹에서 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="d0a35-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d0a35-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a35-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0a35-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="d0a35-109">지정 된 리소스 그룹에서 서비스 버스 네임 스페이스를 제거 `SB-Example1` `Default-ServiceBus-WestUS` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="d0a35-110">변수</span><span class="sxs-lookup"><span data-stu-id="d0a35-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a35-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d0a35-111">-NamespaceName</span></span>
<span data-ttu-id="d0a35-112">Service Bus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-112">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a35-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0a35-113">-ResourceGroup</span></span>
<span data-ttu-id="d0a35-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a35-115">-확인</span><span class="sxs-lookup"><span data-stu-id="d0a35-115">-Confirm</span></span>
<span data-ttu-id="d0a35-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a35-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a35-117">-WhatIf</span></span>
<span data-ttu-id="d0a35-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a35-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a35-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a35-120">CommonParameters</span></span>
<span data-ttu-id="d0a35-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a35-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a35-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a35-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a35-123">입력</span><span class="sxs-lookup"><span data-stu-id="d0a35-123">INPUTS</span></span>

### <span data-ttu-id="d0a35-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0a35-124">-ResourceGroup</span></span>
 <span data-ttu-id="d0a35-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0a35-125">System.String</span></span>

### <span data-ttu-id="d0a35-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d0a35-126">-NamespaceName</span></span>
 <span data-ttu-id="d0a35-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0a35-127">System.String</span></span>

## <span data-ttu-id="d0a35-128">출력</span><span class="sxs-lookup"><span data-stu-id="d0a35-128">OUTPUTS</span></span>

### <span data-ttu-id="d0a35-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d0a35-129">System.Object</span></span>

## <span data-ttu-id="d0a35-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d0a35-130">NOTES</span></span>

## <span data-ttu-id="d0a35-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0a35-131">RELATED LINKS</span></span>

