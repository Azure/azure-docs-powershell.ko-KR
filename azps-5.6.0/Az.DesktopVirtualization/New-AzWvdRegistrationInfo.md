---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966107"
---
# <span data-ttu-id="47e33-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="47e33-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="47e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e33-102">SYNOPSIS</span></span>
<span data-ttu-id="47e33-103">Windows 가상 데스크톱 등록 정보를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="47e33-104">구문</span><span class="sxs-lookup"><span data-stu-id="47e33-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47e33-105">설명</span><span class="sxs-lookup"><span data-stu-id="47e33-105">DESCRIPTION</span></span>
<span data-ttu-id="47e33-106">Windows 가상 데스크톱 등록 정보를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="47e33-107">예제</span><span class="sxs-lookup"><span data-stu-id="47e33-107">EXAMPLES</span></span>

### <span data-ttu-id="47e33-108">예제 1: Windows Virtual Desktop 등록 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="47e33-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="47e33-109">이 명령은 호스트 풀에 Windows Virtual Desktop 등록 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="47e33-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="47e33-110">PARAMETERS</span></span>

### <span data-ttu-id="47e33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e33-111">-DefaultProfile</span></span>
<span data-ttu-id="47e33-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e33-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="47e33-113">-ExpirationTime</span></span>
<span data-ttu-id="47e33-114">만료 시간</span><span class="sxs-lookup"><span data-stu-id="47e33-114">Expiration Time</span></span>

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

### <span data-ttu-id="47e33-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="47e33-115">-HostPoolName</span></span>
<span data-ttu-id="47e33-116">호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="47e33-116">Host Pool Name</span></span>

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

### <span data-ttu-id="47e33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e33-117">-ResourceGroupName</span></span>
<span data-ttu-id="47e33-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="47e33-118">Resource Group Name</span></span>

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

### <span data-ttu-id="47e33-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47e33-119">-SubscriptionId</span></span>
<span data-ttu-id="47e33-120">구독 ID</span><span class="sxs-lookup"><span data-stu-id="47e33-120">Subscription Id</span></span>

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

### <span data-ttu-id="47e33-121">-확인</span><span class="sxs-lookup"><span data-stu-id="47e33-121">-Confirm</span></span>
<span data-ttu-id="47e33-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e33-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e33-123">-WhatIf</span></span>
<span data-ttu-id="47e33-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e33-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e33-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e33-126">CommonParameters</span></span>
<span data-ttu-id="47e33-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47e33-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e33-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47e33-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e33-129">입력</span><span class="sxs-lookup"><span data-stu-id="47e33-129">INPUTS</span></span>

## <span data-ttu-id="47e33-130">출력</span><span class="sxs-lookup"><span data-stu-id="47e33-130">OUTPUTS</span></span>

### <span data-ttu-id="47e33-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="47e33-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="47e33-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47e33-132">NOTES</span></span>

<span data-ttu-id="47e33-133">별칭</span><span class="sxs-lookup"><span data-stu-id="47e33-133">ALIASES</span></span>

## <span data-ttu-id="47e33-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47e33-134">RELATED LINKS</span></span>

