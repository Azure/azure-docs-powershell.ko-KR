---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324337"
---
# <span data-ttu-id="4c5c6-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4c5c6-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="4c5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5c6-103">데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-103">Removes a data share.</span></span>

## <span data-ttu-id="4c5c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c5c6-104">SYNTAX</span></span>

### <span data-ttu-id="4c5c6-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c5c6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5c6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5c6-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c5c6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c5c6-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5c6-108">설명</span><span class="sxs-lookup"><span data-stu-id="4c5c6-108">DESCRIPTION</span></span>
<span data-ttu-id="4c5c6-109">**Remove-AzDataShare** cmdlet은 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="4c5c6-110">예제</span><span class="sxs-lookup"><span data-stu-id="4c5c6-110">EXAMPLES</span></span>

### <span data-ttu-id="4c5c6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c5c6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c5c6-112">이 명령은 Azure 데이터 공유 계정 WikiAds에서 AdsShare라는 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="4c5c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c5c6-113">PARAMETERS</span></span>

### <span data-ttu-id="4c5c6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4c5c6-114">-AccountName</span></span>
<span data-ttu-id="4c5c6-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="4c5c6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4c5c6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c5c6-116">-AsJob</span></span>
<span data-ttu-id="4c5c6-117">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="4c5c6-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4c5c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5c6-118">-DefaultProfile</span></span>
<span data-ttu-id="4c5c6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c5c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c5c6-120">-InputObject</span></span>
<span data-ttu-id="4c5c6-121">Azure 데이터 공유 개체' ''yaml 형식: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="4c5c6-122">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4c5c6-123">-Name</span></span>
<span data-ttu-id="4c5c6-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="4c5c6-124">Azure data share name</span></span>

<span data-ttu-id="4c5c6-125">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4c5c6-126">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c5c6-127">-PassThru</span></span>
<span data-ttu-id="4c5c6-128">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="4c5c6-128">Return object (if specified).</span></span>

<span data-ttu-id="4c5c6-129">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="4c5c6-130">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c5c6-131">-ResourceGroupName</span></span>
<span data-ttu-id="4c5c6-132">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4c5c6-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="4c5c6-133">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4c5c6-134">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c5c6-135">-ResourceId</span></span>
<span data-ttu-id="4c5c6-136">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4c5c6-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="4c5c6-137">yaml 형식: 문자열 매개 변수 집합: ByResourceIdParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="4c5c6-138">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByPropertyName) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c5c6-139">-Confirm</span></span>
<span data-ttu-id="4c5c6-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="4c5c6-141">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: cf</span><span class="sxs-lookup"><span data-stu-id="4c5c6-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="4c5c6-142">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5c6-143">-WhatIf</span></span>
<span data-ttu-id="4c5c6-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4c5c6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c5c6-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-145">The cmdlet is not run.</span></span>

<span data-ttu-id="4c5c6-146">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: wi</span><span class="sxs-lookup"><span data-stu-id="4c5c6-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="4c5c6-147">필수: False 위치: 명명된 기본값: None Accept 파이프라인 입력: False Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="4c5c6-148">yaml 형식: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="4c5c6-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="4c5c6-149">필수: True 위치: 명명된 기본값: None Accept 파이프라인 입력: True(ByValue) Accept 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="4c5c6-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4c5c6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5c6-150">CommonParameters</span></span>
<span data-ttu-id="4c5c6-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5c6-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c5c6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5c6-153">입력</span><span class="sxs-lookup"><span data-stu-id="4c5c6-153">INPUTS</span></span>

### <span data-ttu-id="4c5c6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4c5c6-154">System.String</span></span>

### <span data-ttu-id="4c5c6-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4c5c6-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4c5c6-156">출력</span><span class="sxs-lookup"><span data-stu-id="4c5c6-156">OUTPUTS</span></span>

### <span data-ttu-id="4c5c6-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c5c6-157">System.Boolean</span></span>

## <span data-ttu-id="4c5c6-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c5c6-158">NOTES</span></span>

## <span data-ttu-id="4c5c6-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c5c6-159">RELATED LINKS</span></span>
