---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180201"
---
# <span data-ttu-id="84ed8-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="84ed8-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="84ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="84ed8-103">원격 렌더링 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="84ed8-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="84ed8-104">구문</span><span class="sxs-lookup"><span data-stu-id="84ed8-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84ed8-105">설명</span><span class="sxs-lookup"><span data-stu-id="84ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="84ed8-106">특정 구독, 리소스 그룹 및 지역에 새 원격 렌더링 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="84ed8-107">예제</span><span class="sxs-lookup"><span data-stu-id="84ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="84ed8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="84ed8-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="84ed8-109">현재 구독, 리소스 그룹 "rg1" 및 미국 중부에서 새 원격 렌더링 계정 "예제"를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="84ed8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="84ed8-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84ed8-111">-Confirm</span></span>
<span data-ttu-id="84ed8-112">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ed8-113">-DefaultProfile</span></span>
<span data-ttu-id="84ed8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="84ed8-115">-Location</span></span>
<span data-ttu-id="84ed8-116">원격 렌더링 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="84ed8-117">-Name</span></span>
<span data-ttu-id="84ed8-118">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84ed8-119">-ResourceGroupName</span></span>
<span data-ttu-id="84ed8-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ed8-121">-WhatIf</span></span>
<span data-ttu-id="84ed8-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="84ed8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84ed8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ed8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ed8-124">CommonParameters</span></span>
<span data-ttu-id="84ed8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84ed8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="84ed8-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="84ed8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ed8-127">입력</span><span class="sxs-lookup"><span data-stu-id="84ed8-127">INPUTS</span></span>

### <span data-ttu-id="84ed8-128">없음</span><span class="sxs-lookup"><span data-stu-id="84ed8-128">None</span></span>

## <span data-ttu-id="84ed8-129">출력</span><span class="sxs-lookup"><span data-stu-id="84ed8-129">OUTPUTS</span></span>

### <span data-ttu-id="84ed8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="84ed8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="84ed8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84ed8-131">NOTES</span></span>

## <span data-ttu-id="84ed8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84ed8-132">RELATED LINKS</span></span>
