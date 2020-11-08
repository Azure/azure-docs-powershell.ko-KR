---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204367"
---
# <span data-ttu-id="3d06d-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3d06d-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="3d06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d06d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d06d-103">이 구독에 구성 된 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="3d06d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d06d-104">SYNTAX</span></span>

### <span data-ttu-id="3d06d-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d06d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d06d-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="3d06d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d06d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3d06d-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d06d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d06d-108">DESCRIPTION</span></span>
<span data-ttu-id="3d06d-109">이 구독에 구성 된 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="3d06d-110">보안 담당자는 구독에서 발생 하는 보안 알림에 대 한 알림을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="3d06d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3d06d-111">EXAMPLES</span></span>

### <span data-ttu-id="3d06d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d06d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="3d06d-113">구독에서 구성 된 모든 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="3d06d-114">변수</span><span class="sxs-lookup"><span data-stu-id="3d06d-114">PARAMETERS</span></span>

### <span data-ttu-id="3d06d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d06d-115">-DefaultProfile</span></span>
<span data-ttu-id="3d06d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d06d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3d06d-117">-Name</span></span>
<span data-ttu-id="3d06d-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-118">Resource name.</span></span>

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

### <span data-ttu-id="3d06d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d06d-119">-ResourceId</span></span>
<span data-ttu-id="3d06d-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-120">Resource ID.</span></span>

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

### <span data-ttu-id="3d06d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d06d-121">CommonParameters</span></span>
<span data-ttu-id="3d06d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d06d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d06d-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d06d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d06d-124">입력</span><span class="sxs-lookup"><span data-stu-id="3d06d-124">INPUTS</span></span>

### <span data-ttu-id="3d06d-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d06d-125">System.String</span></span>

## <span data-ttu-id="3d06d-126">출력</span><span class="sxs-lookup"><span data-stu-id="3d06d-126">OUTPUTS</span></span>

### <span data-ttu-id="3d06d-127">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3d06d-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="3d06d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="3d06d-128">NOTES</span></span>

## <span data-ttu-id="3d06d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d06d-129">RELATED LINKS</span></span>
