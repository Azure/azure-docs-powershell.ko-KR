---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200505"
---
# <span data-ttu-id="c87ee-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c87ee-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c87ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c87ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c87ee-103">Windows 가상 데스크톱 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c87ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="c87ee-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c87ee-105">설명</span><span class="sxs-lookup"><span data-stu-id="c87ee-105">DESCRIPTION</span></span>
<span data-ttu-id="c87ee-106">Windows 가상 데스크톱 등록 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c87ee-107">예제</span><span class="sxs-lookup"><span data-stu-id="c87ee-107">EXAMPLES</span></span>

### <span data-ttu-id="c87ee-108">예제 1: Windows Virtual Desktop 등록 토큰을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="c87ee-109">이 명령은 호스트 풀에서 Windows Virtual Desktop 등록 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c87ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c87ee-110">PARAMETERS</span></span>

### <span data-ttu-id="c87ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87ee-111">-DefaultProfile</span></span>
<span data-ttu-id="c87ee-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c87ee-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c87ee-113">-HostPoolName</span></span>
<span data-ttu-id="c87ee-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="c87ee-114">Host Pool Name</span></span>

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

### <span data-ttu-id="c87ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="c87ee-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c87ee-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c87ee-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c87ee-117">-SubscriptionId</span></span>
<span data-ttu-id="c87ee-118">구독 ID</span><span class="sxs-lookup"><span data-stu-id="c87ee-118">Subscription Id</span></span>

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

### <span data-ttu-id="c87ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87ee-119">CommonParameters</span></span>
<span data-ttu-id="c87ee-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c87ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87ee-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c87ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87ee-122">입력</span><span class="sxs-lookup"><span data-stu-id="c87ee-122">INPUTS</span></span>

## <span data-ttu-id="c87ee-123">출력</span><span class="sxs-lookup"><span data-stu-id="c87ee-123">OUTPUTS</span></span>

### <span data-ttu-id="c87ee-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c87ee-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="c87ee-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c87ee-125">NOTES</span></span>

<span data-ttu-id="c87ee-126">별칭</span><span class="sxs-lookup"><span data-stu-id="c87ee-126">ALIASES</span></span>

## <span data-ttu-id="c87ee-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c87ee-127">RELATED LINKS</span></span>

