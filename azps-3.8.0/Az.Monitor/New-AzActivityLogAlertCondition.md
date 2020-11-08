---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042985"
---
# <span data-ttu-id="973de-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="973de-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="973de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="973de-102">SYNOPSIS</span></span>
<span data-ttu-id="973de-103">메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="973de-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="973de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="973de-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="973de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="973de-105">DESCRIPTION</span></span>
<span data-ttu-id="973de-106">**AzActivityLogAlertCondition** cmdlet은 메모리에 새 활동 로그 알림 상태 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="973de-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="973de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="973de-107">EXAMPLES</span></span>

### <span data-ttu-id="973de-108">예제 1: 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="973de-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="973de-109">이 명령은 메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="973de-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="973de-110">**참고** :이 cmdlet을 Set-AzActivityLogAlert에 사용 하는 경우 매개 변수로 전달 되는 이러한 개체 중 하나 이상에는 해당 필드가 "Category"와 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="973de-111">그렇지 않으면 백 엔드가 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="973de-112">변수</span><span class="sxs-lookup"><span data-stu-id="973de-112">PARAMETERS</span></span>

### <span data-ttu-id="973de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973de-113">-DefaultProfile</span></span>
<span data-ttu-id="973de-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="973de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="973de-115">-같음</span><span class="sxs-lookup"><span data-stu-id="973de-115">-Equal</span></span>
<span data-ttu-id="973de-116">리프 조건에 대 한 equals 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="973de-117">-필드</span><span class="sxs-lookup"><span data-stu-id="973de-117">-Field</span></span>
<span data-ttu-id="973de-118">조건에 대 한 필드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="973de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973de-119">CommonParameters</span></span>
<span data-ttu-id="973de-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973de-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="973de-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973de-122">입력</span><span class="sxs-lookup"><span data-stu-id="973de-122">INPUTS</span></span>

### <span data-ttu-id="973de-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="973de-123">System.String</span></span>

## <span data-ttu-id="973de-124">출력</span><span class="sxs-lookup"><span data-stu-id="973de-124">OUTPUTS</span></span>

### <span data-ttu-id="973de-125">ActivityLogAlertLeafCondition를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="973de-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="973de-126">상속자</span><span class="sxs-lookup"><span data-stu-id="973de-126">NOTES</span></span>

## <span data-ttu-id="973de-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="973de-127">RELATED LINKS</span></span>

[<span data-ttu-id="973de-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="973de-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="973de-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="973de-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="973de-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="973de-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="973de-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="973de-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="973de-132">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="973de-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="973de-133">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="973de-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)