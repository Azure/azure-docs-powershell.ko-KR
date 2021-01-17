---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377336"
---
# <span data-ttu-id="b0ea5-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="b0ea5-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="b0ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ea5-103">원본 공유에 대한 해지된 공유 구독 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="b0ea5-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0ea5-104">SYNTAX</span></span>

### <span data-ttu-id="b0ea5-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b0ea5-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0ea5-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0ea5-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0ea5-107">설명</span><span class="sxs-lookup"><span data-stu-id="b0ea5-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ea5-108">**Grant-AzDataShareSubscriptionAccess** cmdlet은 원본 공유에 대한 공유 구독 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="b0ea5-109">예제</span><span class="sxs-lookup"><span data-stu-id="b0ea5-109">EXAMPLES</span></span>

### <span data-ttu-id="b0ea5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0ea5-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="b0ea5-111">ID 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12로 식별된 공유 구독에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="b0ea5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0ea5-112">PARAMETERS</span></span>

### <span data-ttu-id="b0ea5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0ea5-113">-AccountName</span></span>
<span data-ttu-id="b0ea5-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="b0ea5-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b0ea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ea5-115">-DefaultProfile</span></span>
<span data-ttu-id="b0ea5-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ea5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ea5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0ea5-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b0ea5-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b0ea5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0ea5-119">-ResourceId</span></span>
<span data-ttu-id="b0ea5-120">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b0ea5-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="b0ea5-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b0ea5-121">-ShareName</span></span>
<span data-ttu-id="b0ea5-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="b0ea5-122">Azure data share name</span></span>

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

### <span data-ttu-id="b0ea5-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0ea5-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="b0ea5-124">공급자 공유 구독의 공유 구독 ID</span><span class="sxs-lookup"><span data-stu-id="b0ea5-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="b0ea5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0ea5-125">-Confirm</span></span>
<span data-ttu-id="b0ea5-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ea5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0ea5-127">-WhatIf</span></span>
<span data-ttu-id="b0ea5-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b0ea5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0ea5-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ea5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ea5-130">CommonParameters</span></span>
<span data-ttu-id="b0ea5-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ea5-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0ea5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ea5-133">입력</span><span class="sxs-lookup"><span data-stu-id="b0ea5-133">INPUTS</span></span>

### <span data-ttu-id="b0ea5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b0ea5-134">System.String</span></span>

## <span data-ttu-id="b0ea5-135">출력</span><span class="sxs-lookup"><span data-stu-id="b0ea5-135">OUTPUTS</span></span>

### <span data-ttu-id="b0ea5-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b0ea5-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="b0ea5-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0ea5-137">NOTES</span></span>

## <span data-ttu-id="b0ea5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0ea5-138">RELATED LINKS</span></span>
