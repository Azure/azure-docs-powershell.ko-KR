---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344433"
---
# <span data-ttu-id="7a13d-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7a13d-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="7a13d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a13d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a13d-103">Azure Security Center에서 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="7a13d-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="7a13d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a13d-104">SYNTAX</span></span>

### <span data-ttu-id="7a13d-105">GeneralScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a13d-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a13d-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="7a13d-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a13d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a13d-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a13d-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a13d-108">DESCRIPTION</span></span>
<span data-ttu-id="7a13d-109">이 Set-AzSecuritySetting cmdlet은 Azure Security Center에서 특정 보안 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="7a13d-110">예제</span><span class="sxs-lookup"><span data-stu-id="7a13d-110">EXAMPLES</span></span>

### <span data-ttu-id="7a13d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a13d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="7a13d-112">MCAS 데이터 내보내기 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="7a13d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a13d-113">PARAMETERS</span></span>

### <span data-ttu-id="7a13d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a13d-114">-DefaultProfile</span></span>
<span data-ttu-id="7a13d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a13d-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a13d-116">-Enabled</span></span>
<span data-ttu-id="7a13d-117">설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-117">Enables the setting.</span></span>

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

### <span data-ttu-id="7a13d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a13d-118">-InputObject</span></span>
<span data-ttu-id="7a13d-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-119">Input Object.</span></span>

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

### <span data-ttu-id="7a13d-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="7a13d-120">-SettingKind</span></span>
<span data-ttu-id="7a13d-121">설정 종류.</span><span class="sxs-lookup"><span data-stu-id="7a13d-121">Setting kind.</span></span> <span data-ttu-id="7a13d-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="7a13d-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="7a13d-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7a13d-123">-SettingName</span></span>
<span data-ttu-id="7a13d-124">설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-124">Setting name.</span></span> <span data-ttu-id="7a13d-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="7a13d-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="7a13d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a13d-126">-Confirm</span></span>
<span data-ttu-id="7a13d-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a13d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a13d-128">-WhatIf</span></span>
<span data-ttu-id="7a13d-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a13d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a13d-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a13d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a13d-131">CommonParameters</span></span>
<span data-ttu-id="7a13d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a13d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a13d-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a13d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a13d-134">입력</span><span class="sxs-lookup"><span data-stu-id="7a13d-134">INPUTS</span></span>

### <span data-ttu-id="7a13d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7a13d-135">System.String</span></span>
### <span data-ttu-id="7a13d-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7a13d-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="7a13d-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="7a13d-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="7a13d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a13d-138">System.Boolean</span></span>

## <span data-ttu-id="7a13d-139">출력</span><span class="sxs-lookup"><span data-stu-id="7a13d-139">OUTPUTS</span></span>

### <span data-ttu-id="7a13d-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7a13d-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="7a13d-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="7a13d-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="7a13d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a13d-142">NOTES</span></span>

## <span data-ttu-id="7a13d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a13d-143">RELATED LINKS</span></span>
