---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962032"
---
# <span data-ttu-id="e48d3-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e48d3-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="e48d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e48d3-103">Windows 가상 데스크톱 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e48d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e48d3-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e48d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="e48d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e48d3-106">Windows 가상 데스크톱 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e48d3-107">예제</span><span class="sxs-lookup"><span data-stu-id="e48d3-107">EXAMPLES</span></span>

### <span data-ttu-id="e48d3-108">예제 1: Windows Virtual Desktop 등록 토큰을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="e48d3-109">이 명령은 호스트 풀에서 Windows Virtual Desktop 등록 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="e48d3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e48d3-110">PARAMETERS</span></span>

### <span data-ttu-id="e48d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48d3-111">-DefaultProfile</span></span>
<span data-ttu-id="e48d3-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d3-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e48d3-113">-HostPoolName</span></span>
<span data-ttu-id="e48d3-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="e48d3-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="e48d3-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e48d3-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e48d3-117">-SubscriptionId</span></span>
<span data-ttu-id="e48d3-118">구독 ID</span><span class="sxs-lookup"><span data-stu-id="e48d3-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48d3-119">CommonParameters</span></span>
<span data-ttu-id="e48d3-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e48d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48d3-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e48d3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48d3-122">입력</span><span class="sxs-lookup"><span data-stu-id="e48d3-122">INPUTS</span></span>

## <span data-ttu-id="e48d3-123">출력</span><span class="sxs-lookup"><span data-stu-id="e48d3-123">OUTPUTS</span></span>

### <span data-ttu-id="e48d3-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e48d3-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="e48d3-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e48d3-125">NOTES</span></span>

<span data-ttu-id="e48d3-126">별칭</span><span class="sxs-lookup"><span data-stu-id="e48d3-126">ALIASES</span></span>

## <span data-ttu-id="e48d3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e48d3-127">RELATED LINKS</span></span>

