---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 4888cacfbc92a38402bab089555ac6d6e7174038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696699"
---
# <span data-ttu-id="473ca-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="473ca-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="473ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473ca-102">SYNOPSIS</span></span>
<span data-ttu-id="473ca-103">Datashare 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-103">Removes a datashare account</span></span>

## <span data-ttu-id="473ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="473ca-104">SYNTAX</span></span>

### <span data-ttu-id="473ca-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="473ca-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473ca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="473ca-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473ca-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="473ca-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473ca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="473ca-108">DESCRIPTION</span></span>
<span data-ttu-id="473ca-109">**AzDataShareAccount** cmdlet은 datashare account를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="473ca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="473ca-110">EXAMPLES</span></span>

### <span data-ttu-id="473ca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="473ca-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="473ca-112">이 명령은 ADS 라는 리소스 그룹에서 WikiADS 이라는 datashare account를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="473ca-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="473ca-114">변수</span><span class="sxs-lookup"><span data-stu-id="473ca-114">PARAMETERS</span></span>

### <span data-ttu-id="473ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="473ca-115">-AsJob</span></span>
<span data-ttu-id="473ca-116">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="473ca-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="473ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473ca-117">-DefaultProfile</span></span>
<span data-ttu-id="473ca-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473ca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="473ca-119">-Force</span></span>
<span data-ttu-id="473ca-120">{{Force 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="473ca-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="473ca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="473ca-121">-InputObject</span></span>
<span data-ttu-id="473ca-122">Azure data share 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-122">The azure data share account object.</span></span>


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

### <span data-ttu-id="473ca-123">-이름</span><span class="sxs-lookup"><span data-stu-id="473ca-123">-Name</span></span>
<span data-ttu-id="473ca-124">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="473ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="473ca-125">-PassThru</span></span>
<span data-ttu-id="473ca-126">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="473ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="473ca-128">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="473ca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="473ca-129">-ResourceId</span></span>
<span data-ttu-id="473ca-130">Azure data share 계정의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="473ca-131">-확인</span><span class="sxs-lookup"><span data-stu-id="473ca-131">-Confirm</span></span>
<span data-ttu-id="473ca-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473ca-133">-WhatIf</span></span>
<span data-ttu-id="473ca-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="473ca-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="473ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473ca-136">CommonParameters</span></span>
<span data-ttu-id="473ca-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="473ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473ca-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473ca-139">입력</span><span class="sxs-lookup"><span data-stu-id="473ca-139">INPUTS</span></span>

### <span data-ttu-id="473ca-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="473ca-140">System.String</span></span>

### <span data-ttu-id="473ca-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="473ca-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="473ca-142">출력</span><span class="sxs-lookup"><span data-stu-id="473ca-142">OUTPUTS</span></span>

### <span data-ttu-id="473ca-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="473ca-143">System.Boolean</span></span>

## <span data-ttu-id="473ca-144">상속자</span><span class="sxs-lookup"><span data-stu-id="473ca-144">NOTES</span></span>

## <span data-ttu-id="473ca-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="473ca-145">RELATED LINKS</span></span>
