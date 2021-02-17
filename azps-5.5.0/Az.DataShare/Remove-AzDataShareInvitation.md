---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194569"
---
# <span data-ttu-id="bf741-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bf741-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="bf741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf741-102">SYNOPSIS</span></span>
<span data-ttu-id="bf741-103">초대를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-103">removes an invitation</span></span>

## <span data-ttu-id="bf741-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf741-104">SYNTAX</span></span>

### <span data-ttu-id="bf741-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf741-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf741-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf741-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf741-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf741-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf741-108">설명</span><span class="sxs-lookup"><span data-stu-id="bf741-108">DESCRIPTION</span></span>
<span data-ttu-id="bf741-109">**Remove-AzDataShareInvitation** cmdlet은 데이터 공유 초대를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="bf741-110">예제</span><span class="sxs-lookup"><span data-stu-id="bf741-110">EXAMPLES</span></span>

### <span data-ttu-id="bf741-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf741-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="bf741-112">이 명령은 AdsShare 공유에서 ADSInvite라는 초대를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="bf741-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf741-113">PARAMETERS</span></span>

### <span data-ttu-id="bf741-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf741-114">-AccountName</span></span>
<span data-ttu-id="bf741-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="bf741-115">Azure data share account name</span></span>

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

### <span data-ttu-id="bf741-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf741-116">-DefaultProfile</span></span>
<span data-ttu-id="bf741-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf741-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf741-118">-InputObject</span></span>
<span data-ttu-id="bf741-119">Azure 데이터 공유 초대 개체</span><span class="sxs-lookup"><span data-stu-id="bf741-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf741-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf741-120">-Name</span></span>
<span data-ttu-id="bf741-121">Azure 데이터 공유 초대 이름</span><span class="sxs-lookup"><span data-stu-id="bf741-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="bf741-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf741-122">-PassThru</span></span>
<span data-ttu-id="bf741-123">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="bf741-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="bf741-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf741-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf741-125">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bf741-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bf741-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf741-126">-ResourceId</span></span>
<span data-ttu-id="bf741-127">Azure 데이터 공유 초대의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bf741-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="bf741-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bf741-128">-ShareName</span></span>
<span data-ttu-id="bf741-129">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-129">Azure data share name.</span></span>

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

### <span data-ttu-id="bf741-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf741-130">-Confirm</span></span>
<span data-ttu-id="bf741-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf741-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf741-132">-WhatIf</span></span>
<span data-ttu-id="bf741-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bf741-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf741-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf741-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf741-135">CommonParameters</span></span>
<span data-ttu-id="bf741-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf741-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf741-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf741-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf741-138">입력</span><span class="sxs-lookup"><span data-stu-id="bf741-138">INPUTS</span></span>

### <span data-ttu-id="bf741-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bf741-139">System.String</span></span>

### <span data-ttu-id="bf741-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="bf741-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="bf741-141">출력</span><span class="sxs-lookup"><span data-stu-id="bf741-141">OUTPUTS</span></span>

### <span data-ttu-id="bf741-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf741-142">System.Boolean</span></span>

## <span data-ttu-id="bf741-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf741-143">NOTES</span></span>

## <span data-ttu-id="bf741-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf741-144">RELATED LINKS</span></span>
