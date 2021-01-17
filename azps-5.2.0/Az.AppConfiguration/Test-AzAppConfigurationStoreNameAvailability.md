---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323091"
---
# <span data-ttu-id="c26a1-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c26a1-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="c26a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c26a1-103">구성 저장소 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="c26a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c26a1-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c26a1-105">설명</span><span class="sxs-lookup"><span data-stu-id="c26a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c26a1-106">구성 저장소 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="c26a1-107">예제</span><span class="sxs-lookup"><span data-stu-id="c26a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c26a1-108">예제 1: 앱 구성 저장소 이름의 가용성 테스트</span><span class="sxs-lookup"><span data-stu-id="c26a1-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="c26a1-109">이 명령은 앱 구성 저장소 이름의 가용성을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="c26a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c26a1-110">PARAMETERS</span></span>

### <span data-ttu-id="c26a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26a1-111">-DefaultProfile</span></span>
<span data-ttu-id="c26a1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c26a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c26a1-113">-Name</span></span>
<span data-ttu-id="c26a1-114">가용성을 확인할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="c26a1-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c26a1-115">-SubscriptionId</span></span>
<span data-ttu-id="c26a1-116">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26a1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c26a1-117">-Confirm</span></span>
<span data-ttu-id="c26a1-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26a1-119">-WhatIf</span></span>
<span data-ttu-id="c26a1-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c26a1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26a1-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26a1-122">CommonParameters</span></span>
<span data-ttu-id="c26a1-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c26a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26a1-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c26a1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26a1-125">입력</span><span class="sxs-lookup"><span data-stu-id="c26a1-125">INPUTS</span></span>

## <span data-ttu-id="c26a1-126">출력</span><span class="sxs-lookup"><span data-stu-id="c26a1-126">OUTPUTS</span></span>

### <span data-ttu-id="c26a1-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="c26a1-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="c26a1-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c26a1-128">NOTES</span></span>

<span data-ttu-id="c26a1-129">별칭</span><span class="sxs-lookup"><span data-stu-id="c26a1-129">ALIASES</span></span>

## <span data-ttu-id="c26a1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c26a1-130">RELATED LINKS</span></span>

