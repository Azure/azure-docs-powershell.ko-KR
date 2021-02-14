---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203516"
---
# <span data-ttu-id="17afa-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="17afa-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="17afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17afa-102">SYNOPSIS</span></span>
<span data-ttu-id="17afa-103">작업 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-103">Gets action group(s).</span></span>

## <span data-ttu-id="17afa-104">구문</span><span class="sxs-lookup"><span data-stu-id="17afa-104">SYNTAX</span></span>

### <span data-ttu-id="17afa-105">BySubscriptionOrResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="17afa-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17afa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="17afa-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17afa-107">설명</span><span class="sxs-lookup"><span data-stu-id="17afa-107">DESCRIPTION</span></span>
<span data-ttu-id="17afa-108">**Get-AzActionGroup** cmdlet은 하나 이상의 작업 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="17afa-109">예제</span><span class="sxs-lookup"><span data-stu-id="17afa-109">EXAMPLES</span></span>

### <span data-ttu-id="17afa-110">예제 1: 구독 ID로 작업 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="17afa-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="17afa-111">이 명령은 현재 구독에 대한 모든 작업 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="17afa-112">예제 2: 주어진 리소스 그룹에 대한 작업 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="17afa-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="17afa-113">이 명령은 주어진 리소스 그룹에 대한 작업 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="17afa-114">예제 3: 작업 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="17afa-115">이 명령은 하나의 작업 그룹(단일 요소가 있는 목록)을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="17afa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17afa-116">PARAMETERS</span></span>

### <span data-ttu-id="17afa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17afa-117">-DefaultProfile</span></span>
<span data-ttu-id="17afa-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17afa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17afa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="17afa-119">-Name</span></span>
<span data-ttu-id="17afa-120">작업 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-120">The name of the action group.</span></span>

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

### <span data-ttu-id="17afa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17afa-121">-ResourceGroupName</span></span>
<span data-ttu-id="17afa-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="17afa-122">The resource group name</span></span>

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

### <span data-ttu-id="17afa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17afa-123">CommonParameters</span></span>
<span data-ttu-id="17afa-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17afa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17afa-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17afa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17afa-126">입력</span><span class="sxs-lookup"><span data-stu-id="17afa-126">INPUTS</span></span>

### <span data-ttu-id="17afa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="17afa-127">System.String</span></span>

## <span data-ttu-id="17afa-128">출력</span><span class="sxs-lookup"><span data-stu-id="17afa-128">OUTPUTS</span></span>

### <span data-ttu-id="17afa-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="17afa-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="17afa-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17afa-130">NOTES</span></span>

## <span data-ttu-id="17afa-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17afa-131">RELATED LINKS</span></span>

<span data-ttu-id="17afa-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="17afa-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
