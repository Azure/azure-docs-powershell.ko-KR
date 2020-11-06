---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532279"
---
# <span data-ttu-id="510fe-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="510fe-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="510fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="510fe-102">SYNOPSIS</span></span>
<span data-ttu-id="510fe-103">지정 된 이벤트 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="510fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="510fe-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="510fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="510fe-105">DESCRIPTION</span></span>
<span data-ttu-id="510fe-106">Remove-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="510fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="510fe-107">EXAMPLES</span></span>

### <span data-ttu-id="510fe-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="510fe-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="510fe-109">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="510fe-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="510fe-110">변수</span><span class="sxs-lookup"><span data-stu-id="510fe-110">PARAMETERS</span></span>

### <span data-ttu-id="510fe-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510fe-111">-ResourceGroupName</span></span>
<span data-ttu-id="510fe-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-112">Resource group name.</span></span>

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

### <span data-ttu-id="510fe-113">-확인</span><span class="sxs-lookup"><span data-stu-id="510fe-113">-Confirm</span></span>
<span data-ttu-id="510fe-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="510fe-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="510fe-115">-WhatIf</span></span>
<span data-ttu-id="510fe-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="510fe-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="510fe-118">-이름</span><span class="sxs-lookup"><span data-stu-id="510fe-118">-Name</span></span>
<span data-ttu-id="510fe-119">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="510fe-119">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="510fe-120">입력</span><span class="sxs-lookup"><span data-stu-id="510fe-120">INPUTS</span></span>

### <span data-ttu-id="510fe-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="510fe-121">System.String</span></span>

## <span data-ttu-id="510fe-122">출력</span><span class="sxs-lookup"><span data-stu-id="510fe-122">OUTPUTS</span></span>

### <span data-ttu-id="510fe-123">System. 개체</span><span class="sxs-lookup"><span data-stu-id="510fe-123">System.Object</span></span>

## <span data-ttu-id="510fe-124">상속자</span><span class="sxs-lookup"><span data-stu-id="510fe-124">NOTES</span></span>

## <span data-ttu-id="510fe-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="510fe-125">RELATED LINKS</span></span>

