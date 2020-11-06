---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: f690e5d7e35b819b727e2ea3f12c8f5e0b2a375f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524675"
---
# <span data-ttu-id="ecfe8-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecfe8-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="ecfe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfe8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfe8-103">자동화의 DSC 구성을 로컬 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecfe8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecfe8-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfe8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecfe8-105">DESCRIPTION</span></span>
<span data-ttu-id="ecfe8-106">**Export-AzureRmAutomationDscConfiguration** Cmdlet은 Azure 자동화에서 로컬 파일로의 DSC (원하는 상태 구성) 구성을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="ecfe8-107">내보낸 파일의 파일 이름 확장명은. ps1입니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="ecfe8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ecfe8-108">EXAMPLES</span></span>

### <span data-ttu-id="ecfe8-109">예제 1: DSC 구성의 게시 된 버전 내보내기</span><span class="sxs-lookup"><span data-stu-id="ecfe8-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="ecfe8-110">이 명령은 자동화에 있는 DSC 구성의 게시 된 버전을 지정 된 폴더 (바탕 화면)로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="ecfe8-111">변수</span><span class="sxs-lookup"><span data-stu-id="ecfe8-111">PARAMETERS</span></span>

### <span data-ttu-id="ecfe8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ecfe8-112">-AutomationAccountName</span></span>
<span data-ttu-id="ecfe8-113">이 cmdlet이 내보내는 DSC를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="ecfe8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfe8-114">-DefaultProfile</span></span>
<span data-ttu-id="ecfe8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ecfe8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecfe8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ecfe8-116">-Force</span></span>
<span data-ttu-id="ecfe8-117">이 cmdlet이 기존 로컬 파일을 동일한 이름을 가진 새 파일로 대체 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="ecfe8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ecfe8-118">-Name</span></span>
<span data-ttu-id="ecfe8-119">이 cmdlet이 내보내는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe8-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ecfe8-120">-OutputFolder</span></span>
<span data-ttu-id="ecfe8-121">이 cmdlet이 DSC 구성을 내보낼 출력 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="ecfe8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfe8-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecfe8-123">이 cmdlet이 DSC 구성을 내보낼 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="ecfe8-124">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ecfe8-124">-Slot</span></span>
<span data-ttu-id="ecfe8-125">이 cmdlet이 내보내는 DSC 구성 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="ecfe8-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-126">Valid values are:</span></span> 
- <span data-ttu-id="ecfe8-127">함</span><span class="sxs-lookup"><span data-stu-id="ecfe8-127">Draft</span></span>
- <span data-ttu-id="ecfe8-128">게시 된 기본 값이 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfe8-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ecfe8-129">-Confirm</span></span>
<span data-ttu-id="ecfe8-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfe8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfe8-131">-WhatIf</span></span>
<span data-ttu-id="ecfe8-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfe8-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfe8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfe8-134">CommonParameters</span></span>
<span data-ttu-id="ecfe8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecfe8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfe8-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfe8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfe8-137">입력</span><span class="sxs-lookup"><span data-stu-id="ecfe8-137">INPUTS</span></span>

### <span data-ttu-id="ecfe8-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ecfe8-138">System.String</span></span>

## <span data-ttu-id="ecfe8-139">출력</span><span class="sxs-lookup"><span data-stu-id="ecfe8-139">OUTPUTS</span></span>

### <span data-ttu-id="ecfe8-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="ecfe8-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="ecfe8-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ecfe8-141">NOTES</span></span>

## <span data-ttu-id="ecfe8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecfe8-142">RELATED LINKS</span></span>

[<span data-ttu-id="ecfe8-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecfe8-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="ecfe8-144">가져오기-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecfe8-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


