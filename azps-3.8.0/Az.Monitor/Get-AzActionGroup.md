---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: c297198a1e49b93d498c136d1cb099d2068d24db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045006"
---
# <span data-ttu-id="fb9ea-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="fb9ea-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="fb9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9ea-103">작업 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-103">Gets action group(s).</span></span>

## <span data-ttu-id="fb9ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb9ea-104">SYNTAX</span></span>

### <span data-ttu-id="fb9ea-105">BySubscriptionOrResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb9ea-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9ea-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fb9ea-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb9ea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb9ea-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9ea-108">**Get-AzActionGroup** cmdlet은 하나 이상의 작업 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="fb9ea-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb9ea-109">EXAMPLES</span></span>

### <span data-ttu-id="fb9ea-110">예제 1: 구독 ID를 기준으로 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb9ea-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="fb9ea-111">이 명령은 현재 구독에 대 한 모든 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="fb9ea-112">예제 2: 지정 된 리소스 그룹에 대 한 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb9ea-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="fb9ea-113">이 명령은 지정 된 리소스 그룹에 대 한 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="fb9ea-114">예제 3: 작업 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb9ea-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="fb9ea-115">이 명령은 하나 (단일 요소를 포함 하는 목록) 작업 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="fb9ea-116">변수</span><span class="sxs-lookup"><span data-stu-id="fb9ea-116">PARAMETERS</span></span>

### <span data-ttu-id="fb9ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9ea-117">-DefaultProfile</span></span>
<span data-ttu-id="fb9ea-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb9ea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb9ea-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fb9ea-119">-Name</span></span>
<span data-ttu-id="fb9ea-120">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb9ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb9ea-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fb9ea-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9ea-123">CommonParameters</span></span>
<span data-ttu-id="fb9ea-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9ea-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9ea-126">입력</span><span class="sxs-lookup"><span data-stu-id="fb9ea-126">INPUTS</span></span>

### <span data-ttu-id="fb9ea-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb9ea-127">System.String</span></span>

## <span data-ttu-id="fb9ea-128">출력</span><span class="sxs-lookup"><span data-stu-id="fb9ea-128">OUTPUTS</span></span>

### <span data-ttu-id="fb9ea-129">. Psactiongrou보도 정보 클래스.</span><span class="sxs-lookup"><span data-stu-id="fb9ea-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="fb9ea-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fb9ea-130">NOTES</span></span>

## <span data-ttu-id="fb9ea-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb9ea-131">RELATED LINKS</span></span>

<span data-ttu-id="fb9ea-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [제거-AzActionGroup](./Remove-AzActionGroup.md) 
 [새로운 AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="fb9ea-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
