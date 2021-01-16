---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336962"
---
# <span data-ttu-id="09ac1-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="09ac1-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="09ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="09ac1-103">하나 이상의 활동 로그 경고 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="09ac1-104">구문</span><span class="sxs-lookup"><span data-stu-id="09ac1-104">SYNTAX</span></span>

### <span data-ttu-id="09ac1-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09ac1-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09ac1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09ac1-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09ac1-107">설명</span><span class="sxs-lookup"><span data-stu-id="09ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="09ac1-108">**Get-AzActivityLogAlert** cmdlet은 하나 이상의 활동 로그 경고 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="09ac1-109">예제</span><span class="sxs-lookup"><span data-stu-id="09ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="09ac1-110">예제 1: 구독 ID로 활동 로그 경고를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="09ac1-111">이 명령은 현재 구독에 대한 모든 활동 로그 경고를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="09ac1-112">예제 2: 주어진 리소스 그룹에 대한 활동 로그 경고를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="09ac1-113">이 명령은 주어진 리소스 그룹에 대한 활동 로그 경고를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="09ac1-114">예제 3: 활동 로그 경고를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="09ac1-115">이 명령은 하나의(단일 요소가 있는 목록) 활동 로그 경고를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="09ac1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09ac1-116">PARAMETERS</span></span>

### <span data-ttu-id="09ac1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ac1-117">-DefaultProfile</span></span>
<span data-ttu-id="09ac1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="09ac1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ac1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="09ac1-119">-Name</span></span>
<span data-ttu-id="09ac1-120">활동 로그 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ac1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ac1-121">-ResourceGroupName</span></span>
<span data-ttu-id="09ac1-122">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="09ac1-123">Name이 null이 아니거나 비어 있지 않은 경우 이 매개 변수는 비어 있지 않은 문자열을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09ac1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ac1-124">CommonParameters</span></span>
<span data-ttu-id="09ac1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09ac1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ac1-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09ac1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ac1-127">입력</span><span class="sxs-lookup"><span data-stu-id="09ac1-127">INPUTS</span></span>

### <span data-ttu-id="09ac1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="09ac1-128">System.String</span></span>

## <span data-ttu-id="09ac1-129">출력</span><span class="sxs-lookup"><span data-stu-id="09ac1-129">OUTPUTS</span></span>

### <span data-ttu-id="09ac1-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="09ac1-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="09ac1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09ac1-131">NOTES</span></span>

## <span data-ttu-id="09ac1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09ac1-132">RELATED LINKS</span></span>

[<span data-ttu-id="09ac1-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="09ac1-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="09ac1-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="09ac1-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="09ac1-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="09ac1-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="09ac1-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="09ac1-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="09ac1-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="09ac1-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
