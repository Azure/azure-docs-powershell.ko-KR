---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194556"
---
# <span data-ttu-id="f7320-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="f7320-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="f7320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7320-102">SYNOPSIS</span></span>
<span data-ttu-id="f7320-103">동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-103">removes a synchronization setting</span></span>

## <span data-ttu-id="f7320-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7320-104">SYNTAX</span></span>

### <span data-ttu-id="f7320-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f7320-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7320-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7320-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7320-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7320-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7320-108">설명</span><span class="sxs-lookup"><span data-stu-id="f7320-108">DESCRIPTION</span></span>
<span data-ttu-id="f7320-109">**Remove-AzDataShareSynchronizationSetting** cmdlet은 데이터 공유 동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="f7320-110">예제</span><span class="sxs-lookup"><span data-stu-id="f7320-110">EXAMPLES</span></span>

### <span data-ttu-id="f7320-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7320-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f7320-112">이 명령은 AdsShare 공유에서 AdsShareSynchronizationSetting이라는 동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="f7320-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7320-113">PARAMETERS</span></span>

### <span data-ttu-id="f7320-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7320-114">-AccountName</span></span>
<span data-ttu-id="f7320-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="f7320-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="f7320-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7320-116">-AsJob</span></span>
<span data-ttu-id="f7320-117">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="f7320-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f7320-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7320-118">-DefaultProfile</span></span>
<span data-ttu-id="f7320-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7320-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7320-120">-InputObject</span></span>
<span data-ttu-id="f7320-121">Azure 데이터 공유 동기화 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7320-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f7320-122">-Name</span></span>
<span data-ttu-id="f7320-123">동기화 설정 이름</span><span class="sxs-lookup"><span data-stu-id="f7320-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="f7320-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7320-124">-PassThru</span></span>
<span data-ttu-id="f7320-125">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="f7320-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="f7320-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7320-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7320-127">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f7320-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f7320-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7320-128">-ResourceId</span></span>
<span data-ttu-id="f7320-129">동기화 설정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f7320-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="f7320-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f7320-130">-ShareName</span></span>
<span data-ttu-id="f7320-131">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="f7320-131">Azure data share name</span></span>

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

### <span data-ttu-id="f7320-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7320-132">-Confirm</span></span>
<span data-ttu-id="f7320-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7320-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7320-134">-WhatIf</span></span>
<span data-ttu-id="f7320-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f7320-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7320-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7320-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7320-137">CommonParameters</span></span>
<span data-ttu-id="f7320-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7320-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7320-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7320-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7320-140">입력</span><span class="sxs-lookup"><span data-stu-id="f7320-140">INPUTS</span></span>

### <span data-ttu-id="f7320-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f7320-141">System.String</span></span>

### <span data-ttu-id="f7320-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="f7320-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="f7320-143">출력</span><span class="sxs-lookup"><span data-stu-id="f7320-143">OUTPUTS</span></span>

### <span data-ttu-id="f7320-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7320-144">System.Boolean</span></span>

## <span data-ttu-id="f7320-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7320-145">NOTES</span></span>

## <span data-ttu-id="f7320-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7320-146">RELATED LINKS</span></span>
