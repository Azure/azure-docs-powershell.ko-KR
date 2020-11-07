---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 0ff167f14c9a831cb2afe2ce335a0c8bcd18acc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696685"
---
# <span data-ttu-id="2e6f9-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="2e6f9-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2e6f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6f9-103">동기화 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-103">removes a synchronization setting</span></span>

## <span data-ttu-id="2e6f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e6f9-104">SYNTAX</span></span>

### <span data-ttu-id="2e6f9-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e6f9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e6f9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6f9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6f9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6f9-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e6f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2e6f9-108">DESCRIPTION</span></span>
<span data-ttu-id="2e6f9-109">AzDataShareSynchronizationSetting cmdlet은 datashare 동기화 설정을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="2e6f9-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="2e6f9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2e6f9-110">EXAMPLES</span></span>

### <span data-ttu-id="2e6f9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e6f9-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2e6f9-112">이 명령은 AdsShareSynchronizationSetting에서 공유 하는 동기화 설정 (AdsShare)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="2e6f9-113">변수</span><span class="sxs-lookup"><span data-stu-id="2e6f9-113">PARAMETERS</span></span>

### <span data-ttu-id="2e6f9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e6f9-114">-AccountName</span></span>
<span data-ttu-id="2e6f9-115">Azure Data Share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="2e6f9-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="2e6f9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e6f9-116">-AsJob</span></span>
<span data-ttu-id="2e6f9-117">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="2e6f9-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2e6f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6f9-118">-DefaultProfile</span></span>
<span data-ttu-id="2e6f9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6f9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e6f9-120">-InputObject</span></span>
<span data-ttu-id="2e6f9-121">Azure Data Share 동기화 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="2e6f9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2e6f9-122">-Name</span></span>
<span data-ttu-id="2e6f9-123">동기화 설정 이름</span><span class="sxs-lookup"><span data-stu-id="2e6f9-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="2e6f9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e6f9-124">-PassThru</span></span>
<span data-ttu-id="2e6f9-125">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="2e6f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e6f9-127">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e6f9-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2e6f9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e6f9-128">-ResourceId</span></span>
<span data-ttu-id="2e6f9-129">동기화 설정의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2e6f9-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="2e6f9-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2e6f9-130">-ShareName</span></span>
<span data-ttu-id="2e6f9-131">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="2e6f9-131">Azure data share name</span></span>

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

### <span data-ttu-id="2e6f9-132">-확인</span><span class="sxs-lookup"><span data-stu-id="2e6f9-132">-Confirm</span></span>
<span data-ttu-id="2e6f9-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6f9-134">-WhatIf</span></span>
<span data-ttu-id="2e6f9-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6f9-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6f9-137">CommonParameters</span></span>
<span data-ttu-id="2e6f9-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6f9-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6f9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6f9-140">입력</span><span class="sxs-lookup"><span data-stu-id="2e6f9-140">INPUTS</span></span>

### <span data-ttu-id="2e6f9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e6f9-141">System.String</span></span>

### <span data-ttu-id="2e6f9-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="2e6f9-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2e6f9-143">출력</span><span class="sxs-lookup"><span data-stu-id="2e6f9-143">OUTPUTS</span></span>

### <span data-ttu-id="2e6f9-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2e6f9-144">System.Boolean</span></span>

## <span data-ttu-id="2e6f9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="2e6f9-145">NOTES</span></span>

## <span data-ttu-id="2e6f9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e6f9-146">RELATED LINKS</span></span>