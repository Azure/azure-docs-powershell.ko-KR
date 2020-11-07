---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: b16e5a9ff2c6e5a898baf56cf237676665bc12c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696700"
---
# <span data-ttu-id="d81a2-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="d81a2-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="d81a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d81a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d81a2-103">데이터 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-103">Removes a data share.</span></span>

## <span data-ttu-id="d81a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d81a2-104">SYNTAX</span></span>

### <span data-ttu-id="d81a2-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d81a2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81a2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d81a2-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81a2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d81a2-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d81a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d81a2-108">DESCRIPTION</span></span>
<span data-ttu-id="d81a2-109">**제거-AzDataShare** cmdlet은 데이터 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="d81a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d81a2-110">EXAMPLES</span></span>

### <span data-ttu-id="d81a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d81a2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d81a2-112">이 명령은 azure data share 계정 WikiAds에서 AdsShare 라는 데이터 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="d81a2-113">변수</span><span class="sxs-lookup"><span data-stu-id="d81a2-113">PARAMETERS</span></span>

### <span data-ttu-id="d81a2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d81a2-114">-AccountName</span></span>
<span data-ttu-id="d81a2-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-115">Azure data share account name</span></span>

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

### <span data-ttu-id="d81a2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d81a2-116">-AsJob</span></span>
<span data-ttu-id="d81a2-117">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="d81a2-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d81a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81a2-118">-DefaultProfile</span></span>
<span data-ttu-id="d81a2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81a2-120">-InputObject</span></span>
<span data-ttu-id="d81a2-121">Azure data share 개체 ' ' ' yaml 유형: PSDataShare 매개 변수 집합: ByObjectParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="d81a2-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="d81a2-122">필수: 실제 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: True (ByValue) 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-123">-Name</span></span>
<span data-ttu-id="d81a2-124">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-124">Azure data share name</span></span>

<span data-ttu-id="d81a2-125">yaml 유형: String 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="d81a2-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="d81a2-126">필수: 실제 위치: 명명 된 기본값: 수락 파이프라인 입력 허용 안 함: False 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d81a2-127">-PassThru</span></span>
<span data-ttu-id="d81a2-128">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-128">Return object (if specified).</span></span>

<span data-ttu-id="d81a2-129">yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭:</span><span class="sxs-lookup"><span data-stu-id="d81a2-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="d81a2-130">필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81a2-131">-ResourceGroupName</span></span>
<span data-ttu-id="d81a2-132">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="d81a2-133">yaml 유형: String 매개 변수 집합: ByFieldsParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="d81a2-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="d81a2-134">필수: 실제 위치: 명명 된 기본값: 수락 파이프라인 입력 허용 안 함: False 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81a2-135">-ResourceId</span></span>
<span data-ttu-id="d81a2-136">Azure data share의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="d81a2-137">yaml 유형: String 매개 변수 집합: ByResourceIdParameterSet 별칭:</span><span class="sxs-lookup"><span data-stu-id="d81a2-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="d81a2-138">필수: 실제 위치: 명명 된 기본값: 없음 수락 파이프라인 입력: True (ByPropertyName) 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-139">-확인</span><span class="sxs-lookup"><span data-stu-id="d81a2-139">-Confirm</span></span>
<span data-ttu-id="d81a2-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="d81a2-141">yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭: cf</span><span class="sxs-lookup"><span data-stu-id="d81a2-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="d81a2-142">필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>


### <span data-ttu-id="d81a2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81a2-143">-WhatIf</span></span>
<span data-ttu-id="d81a2-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d81a2-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-145">The cmdlet is not run.</span></span>

<span data-ttu-id="d81a2-146">yaml 형식: SwitchParameter 매개 변수 집합: (All) 별칭: wi</span><span class="sxs-lookup"><span data-stu-id="d81a2-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="d81a2-147">필수: False 위치: 명명 된 기본값: 허용 파이프라인 입력 수락 안 함: False 와일드 카드 문자 허용: False</span><span class="sxs-lookup"><span data-stu-id="d81a2-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>
```

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

### <span data-ttu-id="d81a2-148">-이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-148">-Name</span></span>
<span data-ttu-id="d81a2-149">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-149">Azure data share name</span></span>

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

### <span data-ttu-id="d81a2-150">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d81a2-150">-PassThru</span></span>
<span data-ttu-id="d81a2-151">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-151">Return object (if specified).</span></span>

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

### <span data-ttu-id="d81a2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81a2-152">-ResourceGroupName</span></span>
<span data-ttu-id="d81a2-153">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d81a2-153">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d81a2-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81a2-154">-ResourceId</span></span>
<span data-ttu-id="d81a2-155">Azure data share의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-155">The resource id of the Azure data share</span></span>

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

### <span data-ttu-id="d81a2-156">-확인</span><span class="sxs-lookup"><span data-stu-id="d81a2-156">-Confirm</span></span>
<span data-ttu-id="d81a2-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81a2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81a2-158">-WhatIf</span></span>
<span data-ttu-id="d81a2-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d81a2-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81a2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81a2-161">CommonParameters</span></span>
<span data-ttu-id="d81a2-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d81a2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81a2-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81a2-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81a2-164">입력</span><span class="sxs-lookup"><span data-stu-id="d81a2-164">INPUTS</span></span>

### <span data-ttu-id="d81a2-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d81a2-165">System.String</span></span>

### <span data-ttu-id="d81a2-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d81a2-166">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d81a2-167">출력</span><span class="sxs-lookup"><span data-stu-id="d81a2-167">OUTPUTS</span></span>

### <span data-ttu-id="d81a2-168">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d81a2-168">System.Boolean</span></span>

## <span data-ttu-id="d81a2-169">상속자</span><span class="sxs-lookup"><span data-stu-id="d81a2-169">NOTES</span></span>

## <span data-ttu-id="d81a2-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d81a2-170">RELATED LINKS</span></span>
