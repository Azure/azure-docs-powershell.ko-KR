---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189196"
---
# <span data-ttu-id="775d2-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="775d2-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="775d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775d2-102">SYNOPSIS</span></span>
<span data-ttu-id="775d2-103">이 구독에 구성된 보안 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="775d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="775d2-104">SYNTAX</span></span>

### <span data-ttu-id="775d2-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="775d2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="775d2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="775d2-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="775d2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="775d2-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="775d2-108">설명</span><span class="sxs-lookup"><span data-stu-id="775d2-108">DESCRIPTION</span></span>
<span data-ttu-id="775d2-109">이 구독에 구성된 보안 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="775d2-110">보안 연락처는 구독에서 발생 하는 보안 경고에 대한 알림을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="775d2-111">예제</span><span class="sxs-lookup"><span data-stu-id="775d2-111">EXAMPLES</span></span>

### <span data-ttu-id="775d2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="775d2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="775d2-113">구독에서 구성된 모든 보안 연락처를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="775d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="775d2-114">PARAMETERS</span></span>

### <span data-ttu-id="775d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775d2-115">-DefaultProfile</span></span>
<span data-ttu-id="775d2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775d2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="775d2-117">-Name</span></span>
<span data-ttu-id="775d2-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="775d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="775d2-119">-ResourceId</span></span>
<span data-ttu-id="775d2-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="775d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775d2-121">CommonParameters</span></span>
<span data-ttu-id="775d2-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="775d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775d2-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="775d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775d2-124">입력</span><span class="sxs-lookup"><span data-stu-id="775d2-124">INPUTS</span></span>

### <span data-ttu-id="775d2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="775d2-125">System.String</span></span>

## <span data-ttu-id="775d2-126">출력</span><span class="sxs-lookup"><span data-stu-id="775d2-126">OUTPUTS</span></span>

### <span data-ttu-id="775d2-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="775d2-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="775d2-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="775d2-128">NOTES</span></span>

## <span data-ttu-id="775d2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="775d2-129">RELATED LINKS</span></span>
