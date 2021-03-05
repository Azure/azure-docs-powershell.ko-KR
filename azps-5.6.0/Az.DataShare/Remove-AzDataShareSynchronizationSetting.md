---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: c96df19d110a795177d138b7ec34faefb72c0970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966555"
---
# <span data-ttu-id="714f8-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="714f8-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="714f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="714f8-102">SYNOPSIS</span></span>
<span data-ttu-id="714f8-103">동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-103">removes a synchronization setting</span></span>

## <span data-ttu-id="714f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="714f8-104">SYNTAX</span></span>

### <span data-ttu-id="714f8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="714f8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="714f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="714f8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="714f8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="714f8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="714f8-108">설명</span><span class="sxs-lookup"><span data-stu-id="714f8-108">DESCRIPTION</span></span>
<span data-ttu-id="714f8-109">**Remove-AzDataShareSynchronizationSetting** cmdlet은 데이터 공유 동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="714f8-110">예제</span><span class="sxs-lookup"><span data-stu-id="714f8-110">EXAMPLES</span></span>

### <span data-ttu-id="714f8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="714f8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="714f8-112">이 명령은 Share AdsShare에서 AdsShareSynchronizationSetting이라는 동기화 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="714f8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="714f8-113">PARAMETERS</span></span>

### <span data-ttu-id="714f8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="714f8-114">-AccountName</span></span>
<span data-ttu-id="714f8-115">Azure Data Share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="714f8-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="714f8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="714f8-116">-AsJob</span></span>
<span data-ttu-id="714f8-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="714f8-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="714f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714f8-118">-DefaultProfile</span></span>
<span data-ttu-id="714f8-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="714f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="714f8-120">-InputObject</span></span>
<span data-ttu-id="714f8-121">Azure 데이터 공유 동기화 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="714f8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="714f8-122">-Name</span></span>
<span data-ttu-id="714f8-123">동기화 설정 이름</span><span class="sxs-lookup"><span data-stu-id="714f8-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="714f8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="714f8-124">-PassThru</span></span>
<span data-ttu-id="714f8-125">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="714f8-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="714f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="714f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="714f8-127">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="714f8-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="714f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="714f8-128">-ResourceId</span></span>
<span data-ttu-id="714f8-129">동기화 설정의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="714f8-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="714f8-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="714f8-130">-ShareName</span></span>
<span data-ttu-id="714f8-131">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="714f8-131">Azure data share name</span></span>

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

### <span data-ttu-id="714f8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="714f8-132">-Confirm</span></span>
<span data-ttu-id="714f8-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="714f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="714f8-134">-WhatIf</span></span>
<span data-ttu-id="714f8-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="714f8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="714f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714f8-137">CommonParameters</span></span>
<span data-ttu-id="714f8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="714f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714f8-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="714f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714f8-140">입력</span><span class="sxs-lookup"><span data-stu-id="714f8-140">INPUTS</span></span>

### <span data-ttu-id="714f8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="714f8-141">System.String</span></span>

### <span data-ttu-id="714f8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="714f8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="714f8-143">출력</span><span class="sxs-lookup"><span data-stu-id="714f8-143">OUTPUTS</span></span>

### <span data-ttu-id="714f8-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="714f8-144">System.Boolean</span></span>

## <span data-ttu-id="714f8-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="714f8-145">NOTES</span></span>

## <span data-ttu-id="714f8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="714f8-146">RELATED LINKS</span></span>
