---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217311"
---
# <span data-ttu-id="9be58-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="9be58-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="9be58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9be58-102">SYNOPSIS</span></span>
<span data-ttu-id="9be58-103">원격 렌더링 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="9be58-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="9be58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9be58-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9be58-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9be58-105">DESCRIPTION</span></span>
<span data-ttu-id="9be58-106">특정 구독, 리소스 그룹 및 영역에서 새 원격 렌더링 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="9be58-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9be58-107">EXAMPLES</span></span>

### <span data-ttu-id="9be58-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9be58-108">Example 1</span></span>
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

<span data-ttu-id="9be58-109">현재 구독, 리소스 그룹 "rg1" 및 중부 US에 새 원격 렌더링 계정 "예제"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="9be58-110">변수</span><span class="sxs-lookup"><span data-stu-id="9be58-110">PARAMETERS</span></span>

### <span data-ttu-id="9be58-111">-확인</span><span class="sxs-lookup"><span data-stu-id="9be58-111">-Confirm</span></span>
<span data-ttu-id="9be58-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9be58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be58-113">-DefaultProfile</span></span>
<span data-ttu-id="9be58-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9be58-115">-위치</span><span class="sxs-lookup"><span data-stu-id="9be58-115">-Location</span></span>
<span data-ttu-id="9be58-116">원격 렌더링 계정 위치.</span><span class="sxs-lookup"><span data-stu-id="9be58-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="9be58-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9be58-117">-Name</span></span>
<span data-ttu-id="9be58-118">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-118">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="9be58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9be58-119">-ResourceGroupName</span></span>
<span data-ttu-id="9be58-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="9be58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9be58-121">-WhatIf</span></span>
<span data-ttu-id="9be58-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9be58-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9be58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be58-124">CommonParameters</span></span>
<span data-ttu-id="9be58-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9be58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9be58-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be58-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be58-127">입력</span><span class="sxs-lookup"><span data-stu-id="9be58-127">INPUTS</span></span>

### <span data-ttu-id="9be58-128">않아야</span><span class="sxs-lookup"><span data-stu-id="9be58-128">None</span></span>

## <span data-ttu-id="9be58-129">출력</span><span class="sxs-lookup"><span data-stu-id="9be58-129">OUTPUTS</span></span>

### <span data-ttu-id="9be58-130">MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="9be58-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="9be58-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9be58-131">NOTES</span></span>

## <span data-ttu-id="9be58-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9be58-132">RELATED LINKS</span></span>
