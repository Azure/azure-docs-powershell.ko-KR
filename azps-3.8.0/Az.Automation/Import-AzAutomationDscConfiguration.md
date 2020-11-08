---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: 21b3e8c29d9d74f548ca9d212a72d4b70520aa82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044983"
---
# <span data-ttu-id="84bd5-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="84bd5-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="84bd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="84bd5-103">DSC 구성을 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="84bd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84bd5-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84bd5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="84bd5-106">**AzAutomationDscConfiguration** CMDLET은 Ap (원하는 상태의 DSC) 구성을 Azure 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="84bd5-107">단일 DSC 구성을 포함 하는 APS 스크립트의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="84bd5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="84bd5-108">EXAMPLES</span></span>

### <span data-ttu-id="84bd5-109">예제 1: DSC 구성을 자동화로 가져오기</span><span class="sxs-lookup"><span data-stu-id="84bd5-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="84bd5-110">이 명령은 client.ps1 이라는 파일의 DSC 구성을 Contoso17 라는 자동화 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="84bd5-111">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="84bd5-112">기존 DSC 구성이 있는 경우이 명령은 해당 구성을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="84bd5-113">변수</span><span class="sxs-lookup"><span data-stu-id="84bd5-113">PARAMETERS</span></span>

### <span data-ttu-id="84bd5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="84bd5-114">-AutomationAccountName</span></span>
<span data-ttu-id="84bd5-115">이 cmdlet이 DSC 구성을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="84bd5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="84bd5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84bd5-118">-설명</span><span class="sxs-lookup"><span data-stu-id="84bd5-118">-Description</span></span>
<span data-ttu-id="84bd5-119">이 cmdlet이 가져오는 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="84bd5-120">-Force</span></span>
<span data-ttu-id="84bd5-121">이 cmdlet이 자동화의 기존 DSC 구성을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="84bd5-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="84bd5-122">-LogVerbose</span></span>
<span data-ttu-id="84bd5-123">이 DSC 구성의 컴파일 작업에 대해이 cmdlet이 자세한 로깅을 설정 하거나 해제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="84bd5-124">$True의 값을 지정 하 여 자세한 로깅을 설정 하거나 $False 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-125">게시 됨</span><span class="sxs-lookup"><span data-stu-id="84bd5-125">-Published</span></span>
<span data-ttu-id="84bd5-126">이 cmdlet이 게시 된 상태에서 DSC 구성을 가져오는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="84bd5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bd5-127">-ResourceGroupName</span></span>
<span data-ttu-id="84bd5-128">이 cmdlet이 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="84bd5-129">-SourcePath</span></span>
<span data-ttu-id="84bd5-130">이 cmdlet이 가져오는 DSC 구성을 포함 하는 wps_2 스크립트의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-131">태그</span><span class="sxs-lookup"><span data-stu-id="84bd5-131">-Tags</span></span>
<span data-ttu-id="84bd5-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84bd5-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="84bd5-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-134">-확인</span><span class="sxs-lookup"><span data-stu-id="84bd5-134">-Confirm</span></span>
<span data-ttu-id="84bd5-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84bd5-136">-WhatIf</span></span>
<span data-ttu-id="84bd5-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84bd5-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bd5-139">CommonParameters</span></span>
<span data-ttu-id="84bd5-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bd5-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bd5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bd5-142">입력</span><span class="sxs-lookup"><span data-stu-id="84bd5-142">INPUTS</span></span>

### <span data-ttu-id="84bd5-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84bd5-143">System.String</span></span>

### <span data-ttu-id="84bd5-144">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="84bd5-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="84bd5-145">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84bd5-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="84bd5-146">출력</span><span class="sxs-lookup"><span data-stu-id="84bd5-146">OUTPUTS</span></span>

### <span data-ttu-id="84bd5-147">DscConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="84bd5-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="84bd5-148">상속자</span><span class="sxs-lookup"><span data-stu-id="84bd5-148">NOTES</span></span>

## <span data-ttu-id="84bd5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84bd5-149">RELATED LINKS</span></span>

[<span data-ttu-id="84bd5-150">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="84bd5-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="84bd5-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="84bd5-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)
