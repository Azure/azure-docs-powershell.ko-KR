---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377196"
---
# <span data-ttu-id="fffca-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="fffca-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="fffca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fffca-102">SYNOPSIS</span></span>
<span data-ttu-id="fffca-103">데이터 공유 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-103">Removes a datashare account</span></span>

## <span data-ttu-id="fffca-104">구문</span><span class="sxs-lookup"><span data-stu-id="fffca-104">SYNTAX</span></span>

### <span data-ttu-id="fffca-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fffca-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fffca-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fffca-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fffca-108">설명</span><span class="sxs-lookup"><span data-stu-id="fffca-108">DESCRIPTION</span></span>
<span data-ttu-id="fffca-109">**Remove-AzDataShareAccount** cmdlet은 데이터 공유 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="fffca-110">예제</span><span class="sxs-lookup"><span data-stu-id="fffca-110">EXAMPLES</span></span>

### <span data-ttu-id="fffca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fffca-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="fffca-112">이 명령은 ADS라는 리소스 그룹에서 WikiADS라는 데이터 공유 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="fffca-113">이 명령은 $True.</span><span class="sxs-lookup"><span data-stu-id="fffca-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fffca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fffca-114">PARAMETERS</span></span>

### <span data-ttu-id="fffca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fffca-115">-AsJob</span></span>
<span data-ttu-id="fffca-116">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="fffca-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="fffca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffca-117">-DefaultProfile</span></span>
<span data-ttu-id="fffca-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fffca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fffca-119">-Force</span></span>
<span data-ttu-id="fffca-120">{{힘 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="fffca-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="fffca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fffca-121">-InputObject</span></span>
<span data-ttu-id="fffca-122">Azure 데이터 공유 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fffca-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fffca-123">-Name</span></span>
<span data-ttu-id="fffca-124">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="fffca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fffca-125">-PassThru</span></span>
<span data-ttu-id="fffca-126">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="fffca-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="fffca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffca-127">-ResourceGroupName</span></span>
<span data-ttu-id="fffca-128">Azure 데이터 공유 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="fffca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fffca-129">-ResourceId</span></span>
<span data-ttu-id="fffca-130">Azure 데이터 공유 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="fffca-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fffca-131">-Confirm</span></span>
<span data-ttu-id="fffca-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffca-133">-WhatIf</span></span>
<span data-ttu-id="fffca-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fffca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffca-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffca-136">CommonParameters</span></span>
<span data-ttu-id="fffca-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fffca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffca-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fffca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffca-139">입력</span><span class="sxs-lookup"><span data-stu-id="fffca-139">INPUTS</span></span>

### <span data-ttu-id="fffca-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fffca-140">System.String</span></span>

### <span data-ttu-id="fffca-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="fffca-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="fffca-142">출력</span><span class="sxs-lookup"><span data-stu-id="fffca-142">OUTPUTS</span></span>

### <span data-ttu-id="fffca-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fffca-143">System.Boolean</span></span>

## <span data-ttu-id="fffca-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fffca-144">NOTES</span></span>

## <span data-ttu-id="fffca-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fffca-145">RELATED LINKS</span></span>
