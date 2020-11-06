---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537236"
---
# <span data-ttu-id="22e35-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="22e35-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="22e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e35-102">SYNOPSIS</span></span>
<span data-ttu-id="22e35-103">지정 된 이벤트 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22e35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22e35-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="22e35-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22e35-105">DESCRIPTION</span></span>
<span data-ttu-id="22e35-106">Remove-AzureRmEventHub cmdlet은 주어진 네임 스페이스에서 지정 된 이벤트 허브를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="22e35-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22e35-107">EXAMPLES</span></span>

### <span data-ttu-id="22e35-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="22e35-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="22e35-109">이벤트 허브 MyEventHubName를 \` 제거 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="22e35-110">변수</span><span class="sxs-lookup"><span data-stu-id="22e35-110">PARAMETERS</span></span>

### <span data-ttu-id="22e35-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e35-111">-ResourceGroupName</span></span>
<span data-ttu-id="22e35-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-112">Resource group name.</span></span>

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

### <span data-ttu-id="22e35-113">-확인</span><span class="sxs-lookup"><span data-stu-id="22e35-113">-Confirm</span></span>
<span data-ttu-id="22e35-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e35-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e35-115">-WhatIf</span></span>
<span data-ttu-id="22e35-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e35-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e35-118">-이름</span><span class="sxs-lookup"><span data-stu-id="22e35-118">-Name</span></span>
<span data-ttu-id="22e35-119">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="22e35-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e35-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22e35-120">-Namespace</span></span>
<span data-ttu-id="22e35-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22e35-121">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="22e35-122">입력</span><span class="sxs-lookup"><span data-stu-id="22e35-122">INPUTS</span></span>

### <span data-ttu-id="22e35-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22e35-123">System.String</span></span>

## <span data-ttu-id="22e35-124">출력</span><span class="sxs-lookup"><span data-stu-id="22e35-124">OUTPUTS</span></span>

### <span data-ttu-id="22e35-125">System. 개체</span><span class="sxs-lookup"><span data-stu-id="22e35-125">System.Object</span></span>

## <span data-ttu-id="22e35-126">상속자</span><span class="sxs-lookup"><span data-stu-id="22e35-126">NOTES</span></span>

## <span data-ttu-id="22e35-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22e35-127">RELATED LINKS</span></span>

