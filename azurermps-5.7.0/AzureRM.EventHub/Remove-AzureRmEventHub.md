---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537756"
---
# <span data-ttu-id="1837b-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="1837b-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="1837b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1837b-102">SYNOPSIS</span></span>
<span data-ttu-id="1837b-103">지정 된 이벤트 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1837b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1837b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1837b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1837b-105">DESCRIPTION</span></span>
<span data-ttu-id="1837b-106">Remove-AzureRmEventHub cmdlet은 주어진 네임 스페이스에서 지정 된 이벤트 허브를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="1837b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1837b-107">EXAMPLES</span></span>

### <span data-ttu-id="1837b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1837b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="1837b-109">이벤트 허브 MyEventHubName를 \` 제거 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="1837b-110">변수</span><span class="sxs-lookup"><span data-stu-id="1837b-110">PARAMETERS</span></span>

### <span data-ttu-id="1837b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1837b-111">-DefaultProfile</span></span>
<span data-ttu-id="1837b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1837b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="1837b-113">-Name</span></span>
<span data-ttu-id="1837b-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="1837b-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1837b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1837b-115">-Namespace</span></span>
<span data-ttu-id="1837b-116">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1837b-116">Namespace Name</span></span>

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

### <span data-ttu-id="1837b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1837b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1837b-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1837b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1837b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1837b-119">-Confirm</span></span>
<span data-ttu-id="1837b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1837b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1837b-121">-WhatIf</span></span>
<span data-ttu-id="1837b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1837b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1837b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1837b-124">CommonParameters</span></span>
<span data-ttu-id="1837b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1837b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1837b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1837b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1837b-127">입력</span><span class="sxs-lookup"><span data-stu-id="1837b-127">INPUTS</span></span>

### <span data-ttu-id="1837b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1837b-128">System.String</span></span>


## <span data-ttu-id="1837b-129">출력</span><span class="sxs-lookup"><span data-stu-id="1837b-129">OUTPUTS</span></span>

### <span data-ttu-id="1837b-130">System. 개체</span><span class="sxs-lookup"><span data-stu-id="1837b-130">System.Object</span></span>

## <span data-ttu-id="1837b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1837b-131">NOTES</span></span>

## <span data-ttu-id="1837b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1837b-132">RELATED LINKS</span></span>
