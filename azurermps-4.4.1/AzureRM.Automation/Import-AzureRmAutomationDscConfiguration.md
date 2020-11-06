---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531225"
---
# <span data-ttu-id="2889d-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2889d-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="2889d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2889d-102">SYNOPSIS</span></span>
<span data-ttu-id="2889d-103">DSC 구성을 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2889d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2889d-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2889d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2889d-105">DESCRIPTION</span></span>
<span data-ttu-id="2889d-106">**AzureRmAutomationDscConfiguration** CMDLET은 Ap (원하는 상태의 DSC) 구성을 Azure 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="2889d-107">단일 DSC 구성을 포함 하는 APS 스크립트의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="2889d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2889d-108">EXAMPLES</span></span>

### <span data-ttu-id="2889d-109">예제 1: DSC 구성을 자동화로 가져오기</span><span class="sxs-lookup"><span data-stu-id="2889d-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="2889d-110">이 명령은 client.ps1 이라는 파일의 DSC 구성을 Contoso17 라는 자동화 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="2889d-111">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="2889d-112">기존 DSC 구성이 있는 경우이 명령은 해당 구성을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="2889d-113">변수</span><span class="sxs-lookup"><span data-stu-id="2889d-113">PARAMETERS</span></span>

### <span data-ttu-id="2889d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2889d-114">-AutomationAccountName</span></span>
<span data-ttu-id="2889d-115">이 cmdlet이 DSC 구성을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="2889d-116">-설명</span><span class="sxs-lookup"><span data-stu-id="2889d-116">-Description</span></span>
<span data-ttu-id="2889d-117">이 cmdlet이 가져오는 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="2889d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2889d-118">-Force</span></span>
<span data-ttu-id="2889d-119">이 cmdlet이 자동화의 기존 DSC 구성을 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="2889d-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="2889d-120">-LogVerbose</span></span>
<span data-ttu-id="2889d-121">이 DSC 구성의 컴파일 작업에 대해이 cmdlet이 자세한 로깅을 설정 하거나 해제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="2889d-122">$True의 값을 지정 하 여 자세한 로깅을 설정 하거나 $False 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="2889d-123">게시 됨</span><span class="sxs-lookup"><span data-stu-id="2889d-123">-Published</span></span>
<span data-ttu-id="2889d-124">이 cmdlet이 게시 된 상태에서 DSC 구성을 가져오는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="2889d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2889d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2889d-126">이 cmdlet이 DSC 구성을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="2889d-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="2889d-127">-SourcePath</span></span>
<span data-ttu-id="2889d-128">이 cmdlet이 가져오는 DSC 구성을 포함 하는 wps_2 스크립트의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="2889d-129">태그</span><span class="sxs-lookup"><span data-stu-id="2889d-129">-Tags</span></span>
<span data-ttu-id="2889d-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2889d-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="2889d-131">For example:</span></span>

<span data-ttu-id="2889d-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2889d-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2889d-133">-확인</span><span class="sxs-lookup"><span data-stu-id="2889d-133">-Confirm</span></span>
<span data-ttu-id="2889d-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2889d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2889d-135">-WhatIf</span></span>
<span data-ttu-id="2889d-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2889d-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2889d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2889d-138">-DefaultProfile</span></span>
<span data-ttu-id="2889d-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2889d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2889d-140">CommonParameters</span></span>
<span data-ttu-id="2889d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2889d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2889d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2889d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2889d-143">입력</span><span class="sxs-lookup"><span data-stu-id="2889d-143">INPUTS</span></span>

## <span data-ttu-id="2889d-144">출력</span><span class="sxs-lookup"><span data-stu-id="2889d-144">OUTPUTS</span></span>

### <span data-ttu-id="2889d-145">DscConfiguration를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="2889d-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="2889d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="2889d-146">NOTES</span></span>

## <span data-ttu-id="2889d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2889d-147">RELATED LINKS</span></span>

[<span data-ttu-id="2889d-148">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2889d-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="2889d-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2889d-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
