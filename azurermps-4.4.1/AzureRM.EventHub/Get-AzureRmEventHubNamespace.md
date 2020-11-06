---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534959"
---
# <span data-ttu-id="c0210-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c0210-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c0210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0210-102">SYNOPSIS</span></span>
<span data-ttu-id="c0210-103">이벤트 허브 네임 스페이스의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 허브 네임 스페이스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0210-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0210-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="c0210-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c0210-105">DESCRIPTION</span></span>
<span data-ttu-id="c0210-106">Get-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 세부 정보 또는 현재 Azure 구독에서 모든 이벤트 허브 네임 스페이스의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="c0210-107">네임 스페이스 이름을 제공 하는 경우 단일 이벤트 허브 네임 스페이스에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="c0210-108">네임 스페이스 이름을 제공 하지 않으면 네임 스페이스 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="c0210-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0210-109">EXAMPLES</span></span>

### <span data-ttu-id="c0210-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0210-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="c0210-111">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName의 세부 정보를 \` 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="c0210-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c0210-112">변수</span><span class="sxs-lookup"><span data-stu-id="c0210-112">PARAMETERS</span></span>

### <span data-ttu-id="c0210-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0210-113">-ResourceGroupName</span></span>
<span data-ttu-id="c0210-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0210-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c0210-115">-Name</span></span>
<span data-ttu-id="c0210-116">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0210-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c0210-117">입력</span><span class="sxs-lookup"><span data-stu-id="c0210-117">INPUTS</span></span>

### <span data-ttu-id="c0210-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0210-118">System.String</span></span>

## <span data-ttu-id="c0210-119">출력</span><span class="sxs-lookup"><span data-stu-id="c0210-119">OUTPUTS</span></span>

### <span data-ttu-id="c0210-120">System.webserver. List ' 1 [[Microsoft NamespaceAttributes, Microsoft Azure. 0.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="c0210-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c0210-121">상속자</span><span class="sxs-lookup"><span data-stu-id="c0210-121">NOTES</span></span>

## <span data-ttu-id="c0210-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0210-122">RELATED LINKS</span></span>

