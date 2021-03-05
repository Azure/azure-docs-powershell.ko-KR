---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: ea159b52de0dd7d30c898f5119bc819c94d418fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966523"
---
# <span data-ttu-id="b7ac8-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="b7ac8-101">Set-AzDataShare</span></span>

## <span data-ttu-id="b7ac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ac8-103">기존 데이터 공유 업데이트</span><span class="sxs-lookup"><span data-stu-id="b7ac8-103">Updates an existing data share</span></span>

## <span data-ttu-id="b7ac8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7ac8-104">SYNTAX</span></span>

### <span data-ttu-id="b7ac8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7ac8-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ac8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ac8-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ac8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ac8-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ac8-108">설명</span><span class="sxs-lookup"><span data-stu-id="b7ac8-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ac8-109">**Set-AzDataShare** cmdlet은 지정된 Azure 데이터 공유 계정 내에 있는 데이터 공유를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="b7ac8-110">예제</span><span class="sxs-lookup"><span data-stu-id="b7ac8-110">EXAMPLES</span></span>

### <span data-ttu-id="b7ac8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7ac8-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="b7ac8-112">이 명령은 AdsShare라는 기존 데이터 공유를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="b7ac8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7ac8-113">PARAMETERS</span></span>

### <span data-ttu-id="b7ac8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7ac8-114">-AccountName</span></span>
<span data-ttu-id="b7ac8-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="b7ac8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b7ac8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ac8-116">-DefaultProfile</span></span>
<span data-ttu-id="b7ac8-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ac8-118">-Description</span><span class="sxs-lookup"><span data-stu-id="b7ac8-118">-Description</span></span>
<span data-ttu-id="b7ac8-119">데이터 공유에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="b7ac8-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ac8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ac8-120">-InputObject</span></span>
<span data-ttu-id="b7ac8-121">Azure 데이터 공유 개체</span><span class="sxs-lookup"><span data-stu-id="b7ac8-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ac8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ac8-122">-Name</span></span>
<span data-ttu-id="b7ac8-123">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="b7ac8-123">Azure data share name</span></span>

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

### <span data-ttu-id="b7ac8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ac8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7ac8-125">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b7ac8-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b7ac8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ac8-126">-ResourceId</span></span>
<span data-ttu-id="b7ac8-127">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b7ac8-127">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ac8-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="b7ac8-128">-TermsOfUse</span></span>
<span data-ttu-id="b7ac8-129">데이터 공유에 대한 사용 약관</span><span class="sxs-lookup"><span data-stu-id="b7ac8-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ac8-130">-확인</span><span class="sxs-lookup"><span data-stu-id="b7ac8-130">-Confirm</span></span>
<span data-ttu-id="b7ac8-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ac8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ac8-132">-WhatIf</span></span>
<span data-ttu-id="b7ac8-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7ac8-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ac8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ac8-135">CommonParameters</span></span>
<span data-ttu-id="b7ac8-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ac8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ac8-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ac8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ac8-138">입력</span><span class="sxs-lookup"><span data-stu-id="b7ac8-138">INPUTS</span></span>

### <span data-ttu-id="b7ac8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ac8-139">System.String</span></span>

### <span data-ttu-id="b7ac8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b7ac8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b7ac8-141">출력</span><span class="sxs-lookup"><span data-stu-id="b7ac8-141">OUTPUTS</span></span>

### <span data-ttu-id="b7ac8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b7ac8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b7ac8-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7ac8-143">NOTES</span></span>

## <span data-ttu-id="b7ac8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7ac8-144">RELATED LINKS</span></span>
