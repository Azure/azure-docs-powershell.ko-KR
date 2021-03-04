---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: df65bd7b8dfd2f3091590b8830059965e599c029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975723"
---
# <span data-ttu-id="057fb-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="057fb-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="057fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="057fb-102">SYNOPSIS</span></span>
<span data-ttu-id="057fb-103">원격 렌더링 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="057fb-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="057fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="057fb-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="057fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="057fb-105">DESCRIPTION</span></span>
<span data-ttu-id="057fb-106">특정 구독, 리소스 그룹 및 지역에서 새 원격 렌더링 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="057fb-107">예제</span><span class="sxs-lookup"><span data-stu-id="057fb-107">EXAMPLES</span></span>

### <span data-ttu-id="057fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="057fb-108">Example 1</span></span>
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

<span data-ttu-id="057fb-109">현재 구독, 리소스 그룹 "rg1" 및 미국 중부에서 새 원격 렌더링 계정 "예제"를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="057fb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="057fb-110">PARAMETERS</span></span>

### <span data-ttu-id="057fb-111">-확인</span><span class="sxs-lookup"><span data-stu-id="057fb-111">-Confirm</span></span>
<span data-ttu-id="057fb-112">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057fb-113">-DefaultProfile</span></span>
<span data-ttu-id="057fb-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="057fb-115">-Location</span><span class="sxs-lookup"><span data-stu-id="057fb-115">-Location</span></span>
<span data-ttu-id="057fb-116">원격 렌더링 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="057fb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="057fb-117">-Name</span></span>
<span data-ttu-id="057fb-118">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-118">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="057fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="057fb-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="057fb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057fb-121">-WhatIf</span></span>
<span data-ttu-id="057fb-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="057fb-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057fb-124">CommonParameters</span></span>
<span data-ttu-id="057fb-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="057fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="057fb-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="057fb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057fb-127">입력</span><span class="sxs-lookup"><span data-stu-id="057fb-127">INPUTS</span></span>

### <span data-ttu-id="057fb-128">없음</span><span class="sxs-lookup"><span data-stu-id="057fb-128">None</span></span>

## <span data-ttu-id="057fb-129">출력</span><span class="sxs-lookup"><span data-stu-id="057fb-129">OUTPUTS</span></span>

### <span data-ttu-id="057fb-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="057fb-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="057fb-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="057fb-131">NOTES</span></span>

## <span data-ttu-id="057fb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="057fb-132">RELATED LINKS</span></span>
