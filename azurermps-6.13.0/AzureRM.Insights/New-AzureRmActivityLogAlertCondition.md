---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530289"
---
# <span data-ttu-id="ef6d1-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ef6d1-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="ef6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6d1-103">메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef6d1-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef6d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6d1-106">**AzureRmActivityLogAlertCondition** cmdlet은 메모리에 새 활동 로그 알림 상태 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="ef6d1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="ef6d1-108">예제 1: 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="ef6d1-109">이 명령은 메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="ef6d1-110">**참고** :이 cmdlet을 Set-AzureRmActivityLogAlert에 사용 하는 경우 매개 변수로 전달 되는 이러한 개체 중 하나 이상에는 해당 필드가 "Category"와 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="ef6d1-111">그렇지 않으면 백 엔드가 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="ef6d1-112">변수</span><span class="sxs-lookup"><span data-stu-id="ef6d1-112">PARAMETERS</span></span>

### <span data-ttu-id="ef6d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6d1-113">-DefaultProfile</span></span>
<span data-ttu-id="ef6d1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef6d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6d1-115">-같음</span><span class="sxs-lookup"><span data-stu-id="ef6d1-115">-Equal</span></span>
<span data-ttu-id="ef6d1-116">리프 조건에 대 한 equals 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6d1-117">-필드</span><span class="sxs-lookup"><span data-stu-id="ef6d1-117">-Field</span></span>
<span data-ttu-id="ef6d1-118">조건에 대 한 필드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-118">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6d1-119">CommonParameters</span></span>
<span data-ttu-id="ef6d1-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6d1-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6d1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6d1-122">입력</span><span class="sxs-lookup"><span data-stu-id="ef6d1-122">INPUTS</span></span>

### <span data-ttu-id="ef6d1-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef6d1-123">System.String</span></span>

## <span data-ttu-id="ef6d1-124">출력</span><span class="sxs-lookup"><span data-stu-id="ef6d1-124">OUTPUTS</span></span>

### <span data-ttu-id="ef6d1-125">ActivityLogAlertLeafCondition를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef6d1-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="ef6d1-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ef6d1-126">NOTES</span></span>

## <span data-ttu-id="ef6d1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef6d1-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef6d1-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ef6d1-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ef6d1-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ef6d1-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ef6d1-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ef6d1-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ef6d1-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ef6d1-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ef6d1-132">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ef6d1-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ef6d1-133">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ef6d1-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
