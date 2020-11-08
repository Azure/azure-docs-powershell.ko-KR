---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215014"
---
# <span data-ttu-id="2749c-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="2749c-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="2749c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2749c-102">SYNOPSIS</span></span>
<span data-ttu-id="2749c-103">Windows 가상 데스크톱 등록 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="2749c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2749c-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2749c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2749c-105">DESCRIPTION</span></span>
<span data-ttu-id="2749c-106">Windows 가상 데스크톱 등록 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="2749c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2749c-107">EXAMPLES</span></span>

### <span data-ttu-id="2749c-108">예제 1: Windows 가상 데스크톱 등록 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="2749c-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="2749c-109">이 명령은 호스트 풀에 Windows 가상 데스크톱 등록 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="2749c-110">변수</span><span class="sxs-lookup"><span data-stu-id="2749c-110">PARAMETERS</span></span>

### <span data-ttu-id="2749c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2749c-111">-DefaultProfile</span></span>
<span data-ttu-id="2749c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2749c-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="2749c-113">-ExpirationTime</span></span>
<span data-ttu-id="2749c-114">만료 시간</span><span class="sxs-lookup"><span data-stu-id="2749c-114">Expiration Time</span></span>

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

### <span data-ttu-id="2749c-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2749c-115">-HostPoolName</span></span>
<span data-ttu-id="2749c-116">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="2749c-116">Host Pool Name</span></span>

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

### <span data-ttu-id="2749c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2749c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2749c-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2749c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2749c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2749c-119">-SubscriptionId</span></span>
<span data-ttu-id="2749c-120">구독 Id</span><span class="sxs-lookup"><span data-stu-id="2749c-120">Subscription Id</span></span>

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

### <span data-ttu-id="2749c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="2749c-121">-Confirm</span></span>
<span data-ttu-id="2749c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2749c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2749c-123">-WhatIf</span></span>
<span data-ttu-id="2749c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2749c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2749c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2749c-126">CommonParameters</span></span>
<span data-ttu-id="2749c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2749c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2749c-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2749c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2749c-129">입력</span><span class="sxs-lookup"><span data-stu-id="2749c-129">INPUTS</span></span>

## <span data-ttu-id="2749c-130">출력</span><span class="sxs-lookup"><span data-stu-id="2749c-130">OUTPUTS</span></span>

### <span data-ttu-id="2749c-131">Api20191210Preview. i a PowerShell. i i m. i a i. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="2749c-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="2749c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="2749c-132">NOTES</span></span>

<span data-ttu-id="2749c-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="2749c-133">ALIASES</span></span>

## <span data-ttu-id="2749c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2749c-134">RELATED LINKS</span></span>

