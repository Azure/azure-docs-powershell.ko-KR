---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048318"
---
# <span data-ttu-id="ee1ab-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ee1ab-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="ee1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1ab-103">Windows 가상 데스크톱 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ee1ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee1ab-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee1ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1ab-106">Windows 가상 데스크톱 등록 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ee1ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee1ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ee1ab-108">예제 1: Windows 가상 데스크톱 등록 토큰 가져오기</span><span class="sxs-lookup"><span data-stu-id="ee1ab-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="ee1ab-109">이 명령은 호스트 풀에서 Windows 가상 데스크톱 등록 토큰을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="ee1ab-110">변수</span><span class="sxs-lookup"><span data-stu-id="ee1ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ee1ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1ab-111">-DefaultProfile</span></span>
<span data-ttu-id="ee1ab-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1ab-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ee1ab-113">-HostPoolName</span></span>
<span data-ttu-id="ee1ab-114">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="ee1ab-114">Host Pool Name</span></span>

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

### <span data-ttu-id="ee1ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="ee1ab-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ee1ab-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ee1ab-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee1ab-117">-SubscriptionId</span></span>
<span data-ttu-id="ee1ab-118">구독 Id</span><span class="sxs-lookup"><span data-stu-id="ee1ab-118">Subscription Id</span></span>

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

### <span data-ttu-id="ee1ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1ab-119">CommonParameters</span></span>
<span data-ttu-id="ee1ab-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1ab-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1ab-122">입력</span><span class="sxs-lookup"><span data-stu-id="ee1ab-122">INPUTS</span></span>

## <span data-ttu-id="ee1ab-123">출력</span><span class="sxs-lookup"><span data-stu-id="ee1ab-123">OUTPUTS</span></span>

### <span data-ttu-id="ee1ab-124">Api20191210Preview/. i a m.-PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee1ab-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="ee1ab-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ee1ab-125">NOTES</span></span>

<span data-ttu-id="ee1ab-126">별칭과</span><span class="sxs-lookup"><span data-stu-id="ee1ab-126">ALIASES</span></span>

## <span data-ttu-id="ee1ab-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee1ab-127">RELATED LINKS</span></span>

