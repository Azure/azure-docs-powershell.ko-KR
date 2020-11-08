---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204336"
---
# <span data-ttu-id="a6c04-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="a6c04-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="a6c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6c04-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c04-103">Azure 보안 센터에서 보안 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="a6c04-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="a6c04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6c04-104">SYNTAX</span></span>

### <span data-ttu-id="a6c04-105">일반 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a6c04-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c04-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="a6c04-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c04-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c04-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c04-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a6c04-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c04-109">Set-AzSecuritySetting cmdlet은 Azure 보안 센터의 특정 보안 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="a6c04-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a6c04-110">EXAMPLES</span></span>

### <span data-ttu-id="a6c04-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6c04-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="a6c04-112">MCAS 데이터 내보내기 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="a6c04-113">변수</span><span class="sxs-lookup"><span data-stu-id="a6c04-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c04-114">-DefaultProfile</span></span>
<span data-ttu-id="a6c04-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c04-116">-사용</span><span class="sxs-lookup"><span data-stu-id="a6c04-116">-Enabled</span></span>
<span data-ttu-id="a6c04-117">설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-117">Enables the setting.</span></span>

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

### <span data-ttu-id="a6c04-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c04-118">-InputObject</span></span>
<span data-ttu-id="a6c04-119">입력 개체</span><span class="sxs-lookup"><span data-stu-id="a6c04-119">Input Object.</span></span>

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

### <span data-ttu-id="a6c04-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="a6c04-120">-SettingKind</span></span>
<span data-ttu-id="a6c04-121">설정 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-121">Setting kind.</span></span> <span data-ttu-id="a6c04-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="a6c04-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="a6c04-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="a6c04-123">-SettingName</span></span>
<span data-ttu-id="a6c04-124">설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-124">Setting name.</span></span> <span data-ttu-id="a6c04-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="a6c04-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="a6c04-126">-확인</span><span class="sxs-lookup"><span data-stu-id="a6c04-126">-Confirm</span></span>
<span data-ttu-id="a6c04-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c04-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c04-128">-WhatIf</span></span>
<span data-ttu-id="a6c04-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c04-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c04-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c04-131">CommonParameters</span></span>
<span data-ttu-id="a6c04-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c04-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6c04-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c04-134">입력</span><span class="sxs-lookup"><span data-stu-id="a6c04-134">INPUTS</span></span>

### <span data-ttu-id="a6c04-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6c04-135">System.String</span></span>
### <span data-ttu-id="a6c04-136">Microsoft. i. i m/. 설정. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="a6c04-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="a6c04-137">Microsoft. PSSecurityDataExportSetting으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="a6c04-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a6c04-138">System.Boolean</span></span>

## <span data-ttu-id="a6c04-139">출력</span><span class="sxs-lookup"><span data-stu-id="a6c04-139">OUTPUTS</span></span>

### <span data-ttu-id="a6c04-140">Microsoft. i. i m/. 설정. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="a6c04-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="a6c04-141">Microsoft. PSSecurityDataExportSetting으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6c04-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="a6c04-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a6c04-142">NOTES</span></span>

## <span data-ttu-id="a6c04-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6c04-143">RELATED LINKS</span></span>
