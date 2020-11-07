---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703798"
---
# <span data-ttu-id="a95bb-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a95bb-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="a95bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a95bb-103">이 구독에 구성 된 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a95bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a95bb-104">SYNTAX</span></span>

### <span data-ttu-id="a95bb-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a95bb-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a95bb-106">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="a95bb-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a95bb-107">리소스</span><span class="sxs-lookup"><span data-stu-id="a95bb-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a95bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a95bb-108">DESCRIPTION</span></span>
<span data-ttu-id="a95bb-109">이 구독에 구성 된 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="a95bb-110">보안 담당자는 구독에서 발생 하는 보안 알림에 대 한 알림을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="a95bb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a95bb-111">EXAMPLES</span></span>

### <span data-ttu-id="a95bb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a95bb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a95bb-113">구독에서 구성 된 모든 보안 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="a95bb-114">변수</span><span class="sxs-lookup"><span data-stu-id="a95bb-114">PARAMETERS</span></span>

### <span data-ttu-id="a95bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95bb-115">-DefaultProfile</span></span>
<span data-ttu-id="a95bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95bb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a95bb-117">-Name</span></span>
<span data-ttu-id="a95bb-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95bb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a95bb-119">-ResourceId</span></span>
<span data-ttu-id="a95bb-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95bb-121">CommonParameters</span></span>
<span data-ttu-id="a95bb-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95bb-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95bb-124">입력</span><span class="sxs-lookup"><span data-stu-id="a95bb-124">INPUTS</span></span>

### <span data-ttu-id="a95bb-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a95bb-125">System.String</span></span>

## <span data-ttu-id="a95bb-126">출력</span><span class="sxs-lookup"><span data-stu-id="a95bb-126">OUTPUTS</span></span>

### <span data-ttu-id="a95bb-127">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a95bb-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a95bb-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a95bb-128">NOTES</span></span>

## <span data-ttu-id="a95bb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a95bb-129">RELATED LINKS</span></span>
