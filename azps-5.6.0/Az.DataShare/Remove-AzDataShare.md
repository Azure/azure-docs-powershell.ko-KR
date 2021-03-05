---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964731"
---
# <span data-ttu-id="40c08-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="40c08-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="40c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40c08-102">SYNOPSIS</span></span>
<span data-ttu-id="40c08-103">데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-103">Removes a data share.</span></span>

## <span data-ttu-id="40c08-104">구문</span><span class="sxs-lookup"><span data-stu-id="40c08-104">SYNTAX</span></span>

### <span data-ttu-id="40c08-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="40c08-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c08-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c08-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c08-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40c08-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c08-108">설명</span><span class="sxs-lookup"><span data-stu-id="40c08-108">DESCRIPTION</span></span>
<span data-ttu-id="40c08-109">**Remove-AzDataShare** cmdlet은 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="40c08-110">예제</span><span class="sxs-lookup"><span data-stu-id="40c08-110">EXAMPLES</span></span>

### <span data-ttu-id="40c08-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40c08-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="40c08-112">이 명령은 Azure 데이터 공유 계정 WikiAds에서 AdsShare라는 데이터 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="40c08-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40c08-113">PARAMETERS</span></span>

### <span data-ttu-id="40c08-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40c08-114">-AccountName</span></span>
<span data-ttu-id="40c08-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="40c08-115">Azure data share account name</span></span>

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

### <span data-ttu-id="40c08-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c08-116">-AsJob</span></span>
<span data-ttu-id="40c08-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="40c08-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="40c08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c08-118">-DefaultProfile</span></span>
<span data-ttu-id="40c08-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40c08-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c08-120">-InputObject</span></span>
<span data-ttu-id="40c08-121">Azure 데이터 공유 개체' ''yaml 형식: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="40c08-122">필수: True 위치: 명명된 기본값: 없음 수락 파이프라인 입력: True(ByValue) 와일드카드 문자 수락: False</span><span class="sxs-lookup"><span data-stu-id="40c08-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-123">-Name</span><span class="sxs-lookup"><span data-stu-id="40c08-123">-Name</span></span>
<span data-ttu-id="40c08-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="40c08-124">Azure data share name</span></span>

<span data-ttu-id="40c08-125">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="40c08-126">필수: True 위치: 명명된 기본값: 없음 수락 파이프라인 입력: False 수락 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="40c08-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40c08-127">-PassThru</span></span>
<span data-ttu-id="40c08-128">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="40c08-128">Return object (if specified).</span></span>

<span data-ttu-id="40c08-129">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="40c08-130">필수: False 위치: 명명된 기본값: 없음 수락 파이프라인 입력: False 수락 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="40c08-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c08-131">-ResourceGroupName</span></span>
<span data-ttu-id="40c08-132">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="40c08-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="40c08-133">yaml 형식: 문자열 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="40c08-134">필수: True 위치: 명명된 기본값: 없음 수락 파이프라인 입력: False 수락 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="40c08-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40c08-135">-ResourceId</span></span>
<span data-ttu-id="40c08-136">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="40c08-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="40c08-137">yaml 형식: 문자열 매개 변수 집합: ByResourceIdParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="40c08-138">필수: True 위치: 명명된 기본값: 없음 수락 파이프라인 입력: True(ByPropertyName) 와일드카드 문자 수락: False</span><span class="sxs-lookup"><span data-stu-id="40c08-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-139">-확인</span><span class="sxs-lookup"><span data-stu-id="40c08-139">-Confirm</span></span>
<span data-ttu-id="40c08-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="40c08-141">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: cf</span><span class="sxs-lookup"><span data-stu-id="40c08-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="40c08-142">필수: False 위치: 명명된 기본값: 없음 수락 파이프라인 입력: False 수락 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="40c08-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c08-143">-WhatIf</span></span>
<span data-ttu-id="40c08-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c08-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-145">The cmdlet is not run.</span></span>

<span data-ttu-id="40c08-146">yaml 형식: SwitchParameter 매개 변수 집합: (모든) 별칭: wi</span><span class="sxs-lookup"><span data-stu-id="40c08-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="40c08-147">필수: False 위치: 명명된 기본값: 없음 수락 파이프라인 입력: False 수락 와일드카드 문자: False</span><span class="sxs-lookup"><span data-stu-id="40c08-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="40c08-148">yaml 형식: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="40c08-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="40c08-149">필수: True 위치: 명명된 기본값: 없음 수락 파이프라인 입력: True(ByValue) 와일드카드 문자 수락: False</span><span class="sxs-lookup"><span data-stu-id="40c08-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="40c08-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c08-150">CommonParameters</span></span>
<span data-ttu-id="40c08-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40c08-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c08-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40c08-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c08-153">입력</span><span class="sxs-lookup"><span data-stu-id="40c08-153">INPUTS</span></span>

### <span data-ttu-id="40c08-154">System.String</span><span class="sxs-lookup"><span data-stu-id="40c08-154">System.String</span></span>

### <span data-ttu-id="40c08-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="40c08-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="40c08-156">출력</span><span class="sxs-lookup"><span data-stu-id="40c08-156">OUTPUTS</span></span>

### <span data-ttu-id="40c08-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40c08-157">System.Boolean</span></span>

## <span data-ttu-id="40c08-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40c08-158">NOTES</span></span>

## <span data-ttu-id="40c08-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40c08-159">RELATED LINKS</span></span>
