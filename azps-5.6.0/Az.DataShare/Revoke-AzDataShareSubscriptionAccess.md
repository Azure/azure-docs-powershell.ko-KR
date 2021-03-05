---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 3af96fa6ca926c3231d232b641a9d9f5341ea008
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962272"
---
# <span data-ttu-id="f299f-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="f299f-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="f299f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f299f-102">SYNOPSIS</span></span>
<span data-ttu-id="f299f-103">원본 공유에 대한 구독 액세스 해지</span><span class="sxs-lookup"><span data-stu-id="f299f-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="f299f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f299f-104">SYNTAX</span></span>

### <span data-ttu-id="f299f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f299f-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f299f-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f299f-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f299f-107">설명</span><span class="sxs-lookup"><span data-stu-id="f299f-107">DESCRIPTION</span></span>
<span data-ttu-id="f299f-108">**Revoke-AzDataShareSubscriptionAccess** cmdlet은 원본 공유에 대한 공유 구독 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="f299f-109">예제</span><span class="sxs-lookup"><span data-stu-id="f299f-109">EXAMPLES</span></span>

### <span data-ttu-id="f299f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f299f-110">Example 1</span></span>
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

<span data-ttu-id="f299f-111">id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12로 식별된 공유 구독의 액세스 해지</span><span class="sxs-lookup"><span data-stu-id="f299f-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="f299f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f299f-112">PARAMETERS</span></span>

### <span data-ttu-id="f299f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f299f-113">-AccountName</span></span>
<span data-ttu-id="f299f-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="f299f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f299f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f299f-115">-AsJob</span></span>
<span data-ttu-id="f299f-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f299f-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f299f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f299f-117">-DefaultProfile</span></span>
<span data-ttu-id="f299f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f299f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f299f-119">-ResourceGroupName</span></span>
<span data-ttu-id="f299f-120">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f299f-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f299f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f299f-121">-ResourceId</span></span>
<span data-ttu-id="f299f-122">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f299f-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="f299f-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f299f-123">-ShareName</span></span>
<span data-ttu-id="f299f-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="f299f-124">Azure data share name</span></span>

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

### <span data-ttu-id="f299f-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f299f-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="f299f-126">공급자 공유 구독의 공유 구독 ID</span><span class="sxs-lookup"><span data-stu-id="f299f-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="f299f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f299f-127">-Confirm</span></span>
<span data-ttu-id="f299f-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f299f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f299f-129">-WhatIf</span></span>
<span data-ttu-id="f299f-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f299f-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f299f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f299f-132">CommonParameters</span></span>
<span data-ttu-id="f299f-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f299f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f299f-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f299f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f299f-135">입력</span><span class="sxs-lookup"><span data-stu-id="f299f-135">INPUTS</span></span>

### <span data-ttu-id="f299f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f299f-136">System.String</span></span>

## <span data-ttu-id="f299f-137">출력</span><span class="sxs-lookup"><span data-stu-id="f299f-137">OUTPUTS</span></span>

### <span data-ttu-id="f299f-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f299f-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="f299f-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f299f-139">NOTES</span></span>

## <span data-ttu-id="f299f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f299f-140">RELATED LINKS</span></span>
