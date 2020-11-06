---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537175"
---
# <span data-ttu-id="03ef2-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="03ef2-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="03ef2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="03ef2-103">하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ef2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03ef2-104">SYNTAX</span></span>

### <span data-ttu-id="03ef2-105">활동 로그 가져오기 경고에 대 한 기본 매개 변수</span><span class="sxs-lookup"><span data-stu-id="03ef2-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ef2-106">이름을 지정할 때 리소스 그룹이 지정 되었는지 확인 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="03ef2-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03ef2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="03ef2-107">DESCRIPTION</span></span>
<span data-ttu-id="03ef2-108">**Get-AzureRmActivityLogAlert** cmdlet은 하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="03ef2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="03ef2-109">EXAMPLES</span></span>

### <span data-ttu-id="03ef2-110">예제 1: 구독 ID로 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="03ef2-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="03ef2-111">이 명령은 현재 구독에 대 한 모든 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="03ef2-112">예제 2: 지정 된 리소스 그룹에 대 한 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="03ef2-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="03ef2-113">이 명령은 지정 된 리소스 그룹에 대 한 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="03ef2-114">예제 3: 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="03ef2-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="03ef2-115">이 명령은 하나 (단일 요소가 있는 목록) 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="03ef2-116">변수</span><span class="sxs-lookup"><span data-stu-id="03ef2-116">PARAMETERS</span></span>

### <span data-ttu-id="03ef2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="03ef2-117">-Name</span></span>
<span data-ttu-id="03ef2-118">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ef2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ef2-119">-ResourceGroupName</span></span>
<span data-ttu-id="03ef2-120">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="03ef2-121">Name이 null이 아니거나 비어 있지 않은 경우이 매개 변수는 string을 포함 하 고 비어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ef2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ef2-122">-DefaultProfile</span></span>
<span data-ttu-id="03ef2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ef2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ef2-124">CommonParameters</span></span>
<span data-ttu-id="03ef2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03ef2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ef2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ef2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ef2-127">입력</span><span class="sxs-lookup"><span data-stu-id="03ef2-127">INPUTS</span></span>

### <span data-ttu-id="03ef2-128">않아야</span><span class="sxs-lookup"><span data-stu-id="03ef2-128">None</span></span>

## <span data-ttu-id="03ef2-129">출력</span><span class="sxs-lookup"><span data-stu-id="03ef2-129">OUTPUTS</span></span>

### <span data-ttu-id="03ef2-130"><. List ' 1 [Microsoft Azure. e. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="03ef2-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="03ef2-131">않아야</span><span class="sxs-lookup"><span data-stu-id="03ef2-131">None</span></span>

## <span data-ttu-id="03ef2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="03ef2-132">NOTES</span></span>

## <span data-ttu-id="03ef2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03ef2-133">RELATED LINKS</span></span>

[<span data-ttu-id="03ef2-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="03ef2-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="03ef2-135">업데이트-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="03ef2-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="03ef2-136">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="03ef2-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="03ef2-137">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="03ef2-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="03ef2-138">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="03ef2-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
