---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536780"
---
# <span data-ttu-id="ab894-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ab894-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="ab894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab894-102">SYNOPSIS</span></span>
<span data-ttu-id="ab894-103">하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab894-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab894-104">SYNTAX</span></span>

### <span data-ttu-id="ab894-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab894-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab894-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab894-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab894-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab894-107">DESCRIPTION</span></span>
<span data-ttu-id="ab894-108">**Get-AzureRmActivityLogAlert** cmdlet은 하나 이상의 활동 로그 알림 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="ab894-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab894-109">EXAMPLES</span></span>

### <span data-ttu-id="ab894-110">예제 1: 구독 ID로 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab894-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="ab894-111">이 명령은 현재 구독에 대 한 모든 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="ab894-112">예제 2: 지정 된 리소스 그룹에 대 한 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab894-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="ab894-113">이 명령은 지정 된 리소스 그룹에 대 한 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="ab894-114">예제 3: 활동 로그 알림 가져오기</span><span class="sxs-lookup"><span data-stu-id="ab894-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="ab894-115">이 명령은 하나 (단일 요소가 있는 목록) 활동 로그 알림을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="ab894-116">변수</span><span class="sxs-lookup"><span data-stu-id="ab894-116">PARAMETERS</span></span>

### <span data-ttu-id="ab894-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab894-117">-DefaultProfile</span></span>
<span data-ttu-id="ab894-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ab894-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab894-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ab894-119">-Name</span></span>
<span data-ttu-id="ab894-120">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-120">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab894-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab894-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab894-122">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="ab894-123">Name이 null이 아니거나 비어 있지 않은 경우이 매개 변수는 string을 포함 하 고 비어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab894-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab894-124">CommonParameters</span></span>
<span data-ttu-id="ab894-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab894-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab894-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab894-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab894-127">입력</span><span class="sxs-lookup"><span data-stu-id="ab894-127">INPUTS</span></span>

### <span data-ttu-id="ab894-128">않아야</span><span class="sxs-lookup"><span data-stu-id="ab894-128">None</span></span>

## <span data-ttu-id="ab894-129">출력</span><span class="sxs-lookup"><span data-stu-id="ab894-129">OUTPUTS</span></span>

### <span data-ttu-id="ab894-130"><. List ' 1 [Microsoft Azure. e. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="ab894-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="ab894-131">않아야</span><span class="sxs-lookup"><span data-stu-id="ab894-131">None</span></span>

## <span data-ttu-id="ab894-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ab894-132">NOTES</span></span>

## <span data-ttu-id="ab894-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab894-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab894-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ab894-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ab894-135">업데이트-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ab894-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ab894-136">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ab894-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ab894-137">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ab894-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="ab894-138">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ab894-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
