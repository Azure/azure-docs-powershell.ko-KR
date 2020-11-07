---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 26a1fbcc2016de2e6eca4cff2ee2442ef0111919
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867333"
---
# <span data-ttu-id="c161b-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c161b-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="c161b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c161b-102">SYNOPSIS</span></span>
<span data-ttu-id="c161b-103">하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="c161b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c161b-104">SYNTAX</span></span>

### <span data-ttu-id="c161b-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c161b-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c161b-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c161b-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c161b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c161b-107">DESCRIPTION</span></span>
<span data-ttu-id="c161b-108">**Get-AzActivityLogAlert** cmdlet은 하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="c161b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c161b-109">EXAMPLES</span></span>

### <span data-ttu-id="c161b-110">예제 1: 구독 ID로 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="c161b-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="c161b-111">이 명령은 현재 구독에 대 한 모든 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="c161b-112">예제 2: 지정 된 리소스 그룹에 대 한 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="c161b-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="c161b-113">이 명령은 지정 된 리소스 그룹에 대 한 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="c161b-114">예제 3: 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="c161b-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="c161b-115">이 명령은 하나 (단일 요소가 있는 목록) 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="c161b-116">변수</span><span class="sxs-lookup"><span data-stu-id="c161b-116">PARAMETERS</span></span>

### <span data-ttu-id="c161b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c161b-117">-DefaultProfile</span></span>
<span data-ttu-id="c161b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c161b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c161b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c161b-119">-Name</span></span>
<span data-ttu-id="c161b-120">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="c161b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c161b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c161b-122">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="c161b-123">Name이 null이 아니거나 비어 있지 않은 경우이 매개 변수는 string을 포함 하 고 비어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="c161b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c161b-124">CommonParameters</span></span>
<span data-ttu-id="c161b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c161b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c161b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c161b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c161b-127">입력</span><span class="sxs-lookup"><span data-stu-id="c161b-127">INPUTS</span></span>

### <span data-ttu-id="c161b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c161b-128">System.String</span></span>

## <span data-ttu-id="c161b-129">출력</span><span class="sxs-lookup"><span data-stu-id="c161b-129">OUTPUTS</span></span>

### <span data-ttu-id="c161b-130">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c161b-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c161b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c161b-131">NOTES</span></span>

## <span data-ttu-id="c161b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c161b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c161b-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c161b-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c161b-134">업데이트-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c161b-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="c161b-135">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c161b-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="c161b-136">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c161b-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="c161b-137">새로운 AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="c161b-137">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
