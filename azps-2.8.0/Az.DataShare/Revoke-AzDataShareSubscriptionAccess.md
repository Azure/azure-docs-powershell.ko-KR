---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 93e0aa57a418af038a397559959b40500ad58af3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696682"
---
# <span data-ttu-id="3cd13-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="3cd13-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="3cd13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd13-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd13-103">원본 공유에 대 한 공유 구독 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="3cd13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3cd13-104">SYNTAX</span></span>

### <span data-ttu-id="3cd13-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3cd13-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cd13-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cd13-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd13-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3cd13-107">DESCRIPTION</span></span>
<span data-ttu-id="3cd13-108">**AzDataShareSubscriptionAccess** cmdlet은 공유 구독에 원본 공유에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="3cd13-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3cd13-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd13-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cd13-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="3cd13-111">Id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12로 식별 된 공유 구독에 대 한 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="3cd13-112">변수</span><span class="sxs-lookup"><span data-stu-id="3cd13-112">PARAMETERS</span></span>

### <span data-ttu-id="3cd13-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cd13-113">-AccountName</span></span>
<span data-ttu-id="3cd13-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="3cd13-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cd13-115">-AsJob</span></span>
<span data-ttu-id="3cd13-116">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="3cd13-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd13-117">-DefaultProfile</span></span>
<span data-ttu-id="3cd13-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd13-119">-ResourceGroupName</span></span>
<span data-ttu-id="3cd13-120">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3cd13-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd13-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd13-121">-ResourceId</span></span>
<span data-ttu-id="3cd13-122">Azure data share의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-122">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd13-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3cd13-123">-ShareName</span></span>
<span data-ttu-id="3cd13-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="3cd13-124">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd13-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cd13-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="3cd13-126">공급자 공유 구독의 공유 구독 id</span><span class="sxs-lookup"><span data-stu-id="3cd13-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="3cd13-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3cd13-127">-Confirm</span></span>
<span data-ttu-id="3cd13-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd13-129">-WhatIf</span></span>
<span data-ttu-id="3cd13-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cd13-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd13-132">CommonParameters</span></span>
<span data-ttu-id="3cd13-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd13-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd13-135">입력</span><span class="sxs-lookup"><span data-stu-id="3cd13-135">INPUTS</span></span>

### <span data-ttu-id="3cd13-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3cd13-136">System.String</span></span>

## <span data-ttu-id="3cd13-137">출력</span><span class="sxs-lookup"><span data-stu-id="3cd13-137">OUTPUTS</span></span>

### <span data-ttu-id="3cd13-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3cd13-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="3cd13-139">상속자</span><span class="sxs-lookup"><span data-stu-id="3cd13-139">NOTES</span></span>

## <span data-ttu-id="3cd13-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cd13-140">RELATED LINKS</span></span>
