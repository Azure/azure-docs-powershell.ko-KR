---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: a94699bfa4b2637a0d0d51b8f52392bb02f51100
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047819"
---
# <span data-ttu-id="0e112-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="0e112-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="0e112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e112-102">SYNOPSIS</span></span>
<span data-ttu-id="0e112-103">초대를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-103">removes an invitation</span></span>

## <span data-ttu-id="0e112-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e112-104">SYNTAX</span></span>

### <span data-ttu-id="0e112-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e112-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e112-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e112-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e112-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e112-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e112-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0e112-108">DESCRIPTION</span></span>
<span data-ttu-id="0e112-109">**Remove-AzDataShareInvitation** cmdlet은 datashare 초대를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="0e112-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0e112-110">EXAMPLES</span></span>

### <span data-ttu-id="0e112-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e112-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0e112-112">이 명령은 ADSInvite에서 ' 공유 ' 라는 초대를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="0e112-113">변수</span><span class="sxs-lookup"><span data-stu-id="0e112-113">PARAMETERS</span></span>

### <span data-ttu-id="0e112-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0e112-114">-AccountName</span></span>
<span data-ttu-id="0e112-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="0e112-115">Azure data share account name</span></span>

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

### <span data-ttu-id="0e112-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e112-116">-DefaultProfile</span></span>
<span data-ttu-id="0e112-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e112-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e112-118">-InputObject</span></span>
<span data-ttu-id="0e112-119">Azure data share 초대 개체</span><span class="sxs-lookup"><span data-stu-id="0e112-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="0e112-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0e112-120">-Name</span></span>
<span data-ttu-id="0e112-121">Azure data share 초대 이름</span><span class="sxs-lookup"><span data-stu-id="0e112-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="0e112-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e112-122">-PassThru</span></span>
<span data-ttu-id="0e112-123">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="0e112-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e112-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e112-125">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0e112-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0e112-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e112-126">-ResourceId</span></span>
<span data-ttu-id="0e112-127">Azure data share 초대의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="0e112-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0e112-128">-ShareName</span></span>
<span data-ttu-id="0e112-129">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-129">Azure data share name.</span></span>

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

### <span data-ttu-id="0e112-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0e112-130">-Confirm</span></span>
<span data-ttu-id="0e112-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e112-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e112-132">-WhatIf</span></span>
<span data-ttu-id="0e112-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e112-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e112-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e112-135">CommonParameters</span></span>
<span data-ttu-id="0e112-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e112-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e112-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e112-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e112-138">입력</span><span class="sxs-lookup"><span data-stu-id="0e112-138">INPUTS</span></span>

### <span data-ttu-id="0e112-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e112-139">System.String</span></span>

### <span data-ttu-id="0e112-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="0e112-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="0e112-141">출력</span><span class="sxs-lookup"><span data-stu-id="0e112-141">OUTPUTS</span></span>

### <span data-ttu-id="0e112-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0e112-142">System.Boolean</span></span>

## <span data-ttu-id="0e112-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0e112-143">NOTES</span></span>

## <span data-ttu-id="0e112-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e112-144">RELATED LINKS</span></span>
