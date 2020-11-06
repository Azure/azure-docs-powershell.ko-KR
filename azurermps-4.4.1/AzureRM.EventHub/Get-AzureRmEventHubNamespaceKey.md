---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537252"
---
# <span data-ttu-id="1f5d4-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="1f5d4-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="1f5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5d4-103">지정 된 이벤트 허브 네임 스페이스 권한 부여 규칙의 권한 부여 규칙에 대 한 기본, 보조 connectionstrings 및 키의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f5d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f5d4-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="1f5d4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="1f5d4-106">Get-AzureRmEventHubNamespaceKey cmdlet은 지정 된 이벤트 허브 네임 스페이스에서 지정한 권한 부여 규칙의 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="1f5d4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="1f5d4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f5d4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="1f5d4-109">\` \` \` \` 리소스 그룹 MyResourceGroupName의 이벤트 허브 네임 스페이스 MyNamespaceName에서 권한 \` 부여 규칙 MyAuthRuleName에 대 한 기본, 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="1f5d4-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1f5d4-110">변수</span><span class="sxs-lookup"><span data-stu-id="1f5d4-110">PARAMETERS</span></span>

### <span data-ttu-id="1f5d4-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="1f5d4-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="1f5d4-112">이벤트 허브 네임 스페이스에 대 한 권한 부여 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f5d4-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1f5d4-113">-NamespaceName</span></span>
<span data-ttu-id="1f5d4-114">이벤트 허브 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="1f5d4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5d4-115">-ResourceGroupName</span></span>
<span data-ttu-id="1f5d4-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-116">Resource group name.</span></span>

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

## <span data-ttu-id="1f5d4-117">입력</span><span class="sxs-lookup"><span data-stu-id="1f5d4-117">INPUTS</span></span>

### <span data-ttu-id="1f5d4-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f5d4-118">System.String</span></span>

## <span data-ttu-id="1f5d4-119">출력</span><span class="sxs-lookup"><span data-stu-id="1f5d4-119">OUTPUTS</span></span>

### <span data-ttu-id="1f5d4-120">ListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="1f5d4-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="1f5d4-121">상속자</span><span class="sxs-lookup"><span data-stu-id="1f5d4-121">NOTES</span></span>

## <span data-ttu-id="1f5d4-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f5d4-122">RELATED LINKS</span></span>

