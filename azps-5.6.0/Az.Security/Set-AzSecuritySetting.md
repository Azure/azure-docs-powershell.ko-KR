---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 5c7e9d80ffd9109cda1f13f74b1febb3b28e10ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005744"
---
# <span data-ttu-id="eda74-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="eda74-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="eda74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda74-102">SYNOPSIS</span></span>
<span data-ttu-id="eda74-103">Azure Security Center에서 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="eda74-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="eda74-104">구문</span><span class="sxs-lookup"><span data-stu-id="eda74-104">SYNTAX</span></span>

### <span data-ttu-id="eda74-105">GeneralScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="eda74-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eda74-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="eda74-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eda74-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eda74-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda74-108">설명</span><span class="sxs-lookup"><span data-stu-id="eda74-108">DESCRIPTION</span></span>
<span data-ttu-id="eda74-109">Set-AzSecuritySetting cmdlet은 Azure Security Center에서 특정 보안 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="eda74-110">예제</span><span class="sxs-lookup"><span data-stu-id="eda74-110">EXAMPLES</span></span>

### <span data-ttu-id="eda74-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="eda74-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="eda74-112">MCAS 데이터 내보내기 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="eda74-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="eda74-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eda74-113">PARAMETERS</span></span>

### <span data-ttu-id="eda74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda74-114">-DefaultProfile</span></span>
<span data-ttu-id="eda74-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda74-116">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="eda74-116">-Enabled</span></span>
<span data-ttu-id="eda74-117">설정을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda74-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eda74-118">-InputObject</span></span>
<span data-ttu-id="eda74-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eda74-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="eda74-120">-SettingKind</span></span>
<span data-ttu-id="eda74-121">종류를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-121">Setting kind.</span></span> <span data-ttu-id="eda74-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="eda74-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda74-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="eda74-123">-SettingName</span></span>
<span data-ttu-id="eda74-124">이름 설정.</span><span class="sxs-lookup"><span data-stu-id="eda74-124">Setting name.</span></span> <span data-ttu-id="eda74-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="eda74-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda74-126">-확인</span><span class="sxs-lookup"><span data-stu-id="eda74-126">-Confirm</span></span>
<span data-ttu-id="eda74-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda74-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda74-128">-WhatIf</span></span>
<span data-ttu-id="eda74-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda74-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda74-131">CommonParameters</span></span>
<span data-ttu-id="eda74-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eda74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda74-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eda74-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda74-134">입력</span><span class="sxs-lookup"><span data-stu-id="eda74-134">INPUTS</span></span>

### <span data-ttu-id="eda74-135">System.String</span><span class="sxs-lookup"><span data-stu-id="eda74-135">System.String</span></span>
### <span data-ttu-id="eda74-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="eda74-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="eda74-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="eda74-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="eda74-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eda74-138">System.Boolean</span></span>

## <span data-ttu-id="eda74-139">출력</span><span class="sxs-lookup"><span data-stu-id="eda74-139">OUTPUTS</span></span>

### <span data-ttu-id="eda74-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="eda74-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="eda74-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="eda74-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="eda74-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eda74-142">NOTES</span></span>

## <span data-ttu-id="eda74-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eda74-143">RELATED LINKS</span></span>
