---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373549"
---
# <span data-ttu-id="fcbca-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbca-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="fcbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbca-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbca-103">모듈을 Automation으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="fcbca-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="fcbca-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcbca-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbca-105">설명</span><span class="sxs-lookup"><span data-stu-id="fcbca-105">DESCRIPTION</span></span>
<span data-ttu-id="fcbca-106">**New-AzAutomationModule** cmdlet은 모듈을 Azure Automation으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="fcbca-107">이 명령은 .zip 파일 이름 확장명을 사용하는 압축 파일을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="fcbca-108">파일에는 다음 형식 중 하나인 파일이 포함된 폴더가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="fcbca-109">Windows PowerShell .psm1 또는 .dll 파일 이름 확장명이 있는 모듈</span><span class="sxs-lookup"><span data-stu-id="fcbca-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="fcbca-110">Windows PowerShell .psd1 파일 이름 확장명을 품은 모듈 매니페스트는 .zip 파일의 이름, 폴더의 이름 및 폴더의 파일 이름이 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="fcbca-111">.zip 파일을 Automation 서비스에서 액세스할 수 있는 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="fcbca-112">이 cmdlet 또는 Windows PowerShell cmdlet을 사용하여 Automation에 Set-AzAutomationModule 모듈을 가져오는 경우 작업은 비동기적입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="fcbca-113">이 명령은 가져오기 성공 또는 실패 여부를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="fcbca-114">성공 여부를 확인하기 위해 다음 명령을 실행합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName은 **ProvisioningState** 속성을 확인하여 Succeeded 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="fcbca-115">예제</span><span class="sxs-lookup"><span data-stu-id="fcbca-115">EXAMPLES</span></span>

### <span data-ttu-id="fcbca-116">예제 1: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="fcbca-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fcbca-117">이 명령은 ContosoModule이라는 모듈을 Contoso17이라는 Automation 계정으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="fcbca-118">모듈은 contosostorage라는 스토리지 계정 및 모듈이라는 컨테이너의 Azure Blob에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="fcbca-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcbca-119">PARAMETERS</span></span>

### <span data-ttu-id="fcbca-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fcbca-120">-AutomationAccountName</span></span>
<span data-ttu-id="fcbca-121">이 cmdlet이 모듈을 가져오는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fcbca-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="fcbca-122">-ContentLinkUri</span></span>
<span data-ttu-id="fcbca-123">모듈 zip 패키지에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbca-124">-DefaultProfile</span></span>
<span data-ttu-id="fcbca-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcbca-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcbca-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fcbca-126">-Name</span></span>
<span data-ttu-id="fcbca-127">이 cmdlet에서 가져오는 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-127">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbca-128">-ResourceGroupName</span></span>
<span data-ttu-id="fcbca-129">이 cmdlet이 모듈을 가져올 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fcbca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbca-130">CommonParameters</span></span>
<span data-ttu-id="fcbca-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbca-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fcbca-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbca-133">입력</span><span class="sxs-lookup"><span data-stu-id="fcbca-133">INPUTS</span></span>

### <span data-ttu-id="fcbca-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fcbca-134">System.String</span></span>

### <span data-ttu-id="fcbca-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="fcbca-135">System.Uri</span></span>

## <span data-ttu-id="fcbca-136">출력</span><span class="sxs-lookup"><span data-stu-id="fcbca-136">OUTPUTS</span></span>

### <span data-ttu-id="fcbca-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="fcbca-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="fcbca-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcbca-138">NOTES</span></span>

## <span data-ttu-id="fcbca-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcbca-139">RELATED LINKS</span></span>

[<span data-ttu-id="fcbca-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbca-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="fcbca-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbca-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="fcbca-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbca-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


