---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338169"
---
# <span data-ttu-id="5b2b9-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5b2b9-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="5b2b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2b9-103">메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="5b2b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b2b9-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="5b2b9-106">**New-AzActivityLogAlertCondition cmdlet은** 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="5b2b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b2b9-107">EXAMPLES</span></span>

### <span data-ttu-id="5b2b9-108">예제 1: 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="5b2b9-109">이 명령은 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="5b2b9-110">**참고:** 이 cmdlet을 [Set-AzActivityLogAlert에](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) 매개 변수로 전달된 이러한 개체 중 하나 이상과 함께 사용하는 경우 해당 필드가 "Category"와 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="5b2b9-111">그렇지 않으면 백에는 400(BadRequest)으로 응답합니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="5b2b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b2b9-112">PARAMETERS</span></span>

### <span data-ttu-id="5b2b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2b9-113">-DefaultProfile</span></span>
<span data-ttu-id="5b2b9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5b2b9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b2b9-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="5b2b9-115">-Equal</span></span>
<span data-ttu-id="5b2b9-116">리프 조건에 대한 equals 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="5b2b9-117">-Field</span><span class="sxs-lookup"><span data-stu-id="5b2b9-117">-Field</span></span>
<span data-ttu-id="5b2b9-118">조건에 대한 필드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="5b2b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2b9-119">CommonParameters</span></span>
<span data-ttu-id="5b2b9-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2b9-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b2b9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2b9-122">입력</span><span class="sxs-lookup"><span data-stu-id="5b2b9-122">INPUTS</span></span>

### <span data-ttu-id="5b2b9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5b2b9-123">System.String</span></span>

## <span data-ttu-id="5b2b9-124">출력</span><span class="sxs-lookup"><span data-stu-id="5b2b9-124">OUTPUTS</span></span>

### <span data-ttu-id="5b2b9-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="5b2b9-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="5b2b9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b2b9-126">NOTES</span></span>

## <span data-ttu-id="5b2b9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b2b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b2b9-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b2b9-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="5b2b9-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b2b9-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="5b2b9-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b2b9-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="5b2b9-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b2b9-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="5b2b9-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b2b9-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="5b2b9-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="5b2b9-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
