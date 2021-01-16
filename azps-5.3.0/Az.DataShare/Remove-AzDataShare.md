---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377203"
---
# <span data-ttu-id="c50f0-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="c50f0-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="c50f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c50f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c50f0-103">데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-103">Removes a data share.</span></span>

## <span data-ttu-id="c50f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="c50f0-104">SYNTAX</span></span>

### <span data-ttu-id="c50f0-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c50f0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c50f0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c50f0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c50f0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c50f0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c50f0-108">설명</span><span class="sxs-lookup"><span data-stu-id="c50f0-108">DESCRIPTION</span></span>
<span data-ttu-id="c50f0-109">**Remove-AzDataShare** cmdlet은 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="c50f0-110">예제</span><span class="sxs-lookup"><span data-stu-id="c50f0-110">EXAMPLES</span></span>

### <span data-ttu-id="c50f0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c50f0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c50f0-112">이 명령은 Azure 데이터 공유 계정 WikiAds에서 AdsShare라는 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="c50f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c50f0-113">PARAMETERS</span></span>

### <span data-ttu-id="c50f0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c50f0-114">-AccountName</span></span>
<span data-ttu-id="c50f0-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="c50f0-115">Azure data share account name</span></span>

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

### <span data-ttu-id="c50f0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c50f0-116">-AsJob</span></span>
<span data-ttu-id="c50f0-117">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="c50f0-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c50f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50f0-118">-DefaultProfile</span></span>
<span data-ttu-id="c50f0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c50f0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c50f0-120">-InputObject</span></span>
<span data-ttu-id="c50f0-121">Azure 데이터 공유 개체' ''yaml 형식: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="c50f0-122">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c50f0-123">-Name</span></span>
<span data-ttu-id="c50f0-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="c50f0-124">Azure data share name</span></span>

<span data-ttu-id="c50f0-125">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="c50f0-126">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c50f0-127">-PassThru</span></span>
<span data-ttu-id="c50f0-128">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="c50f0-128">Return object (if specified).</span></span>

<span data-ttu-id="c50f0-129">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="c50f0-130">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c50f0-131">-ResourceGroupName</span></span>
<span data-ttu-id="c50f0-132">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c50f0-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="c50f0-133">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="c50f0-134">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c50f0-135">-ResourceId</span></span>
<span data-ttu-id="c50f0-136">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c50f0-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="c50f0-137">yaml 형식: 문자열 매개 변수 집합: ByResourceIdParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="c50f0-138">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByPropertyName) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c50f0-139">-Confirm</span></span>
<span data-ttu-id="c50f0-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="c50f0-141">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: cf</span><span class="sxs-lookup"><span data-stu-id="c50f0-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="c50f0-142">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c50f0-143">-WhatIf</span></span>
<span data-ttu-id="c50f0-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c50f0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c50f0-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-145">The cmdlet is not run.</span></span>

<span data-ttu-id="c50f0-146">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: wi</span><span class="sxs-lookup"><span data-stu-id="c50f0-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="c50f0-147">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="c50f0-148">yaml 형식: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="c50f0-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="c50f0-149">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="c50f0-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="c50f0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50f0-150">CommonParameters</span></span>
<span data-ttu-id="c50f0-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c50f0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50f0-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c50f0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50f0-153">입력</span><span class="sxs-lookup"><span data-stu-id="c50f0-153">INPUTS</span></span>

### <span data-ttu-id="c50f0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c50f0-154">System.String</span></span>

### <span data-ttu-id="c50f0-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="c50f0-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="c50f0-156">출력</span><span class="sxs-lookup"><span data-stu-id="c50f0-156">OUTPUTS</span></span>

### <span data-ttu-id="c50f0-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c50f0-157">System.Boolean</span></span>

## <span data-ttu-id="c50f0-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c50f0-158">NOTES</span></span>

## <span data-ttu-id="c50f0-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c50f0-159">RELATED LINKS</span></span>
