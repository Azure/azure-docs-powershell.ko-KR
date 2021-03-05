---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012731"
---
# <span data-ttu-id="f6ff8-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f6ff8-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="f6ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ff8-103">모듈을 Automation로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="f6ff8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6ff8-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ff8-105">설명</span><span class="sxs-lookup"><span data-stu-id="f6ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ff8-106">**New-AzAutomationModule** cmdlet은 모듈을 Azure Automation으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="f6ff8-107">이 명령은 .zip 파일 이름 확장이 있는 압축된 파일을 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="f6ff8-108">파일에는 다음 형식 중 하나인 파일이 포함된 폴더가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="f6ff8-109">.psm1 또는 .dll 파일 이름 확장이 있는 Windows PowerShell 모듈</span><span class="sxs-lookup"><span data-stu-id="f6ff8-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="f6ff8-110">Windows PowerShell 모듈 매니페스트에는 .psd1 파일 이름 확장명 .zip 파일의 이름, 폴더의 이름 및 폴더의 파일의 이름이 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="f6ff8-111">.zip 파일을 Automation 서비스가 액세스할 수 있는 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="f6ff8-112">이 cmdlet 또는 Windows PowerShell cmdlet을 사용하여 automation에 Set-AzAutomationModule 모듈을 가져오는 경우 작업은 비동기입니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="f6ff8-113">명령은 가져오기 성공 여부와 실패 여부를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="f6ff8-114">성공 여부를 확인한 다음 명령을 `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` 실행합니다. ModuleName이 **ProvisioningState** 속성을 성공한 값으로 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="f6ff8-115">예제</span><span class="sxs-lookup"><span data-stu-id="f6ff8-115">EXAMPLES</span></span>

### <span data-ttu-id="f6ff8-116">예제 1: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6ff8-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f6ff8-117">이 명령은 ContosoModule이라는 모듈을 Contoso17이라는 Automation 계정으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="f6ff8-118">모듈은 contosostorage라는 저장소 계정의 Azure Blob 및 모듈이라는 컨테이너에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="f6ff8-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6ff8-119">PARAMETERS</span></span>

### <span data-ttu-id="f6ff8-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6ff8-120">-AutomationAccountName</span></span>
<span data-ttu-id="f6ff8-121">이 cmdlet에서 모듈을 가져오는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="f6ff8-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="f6ff8-122">-ContentLinkUri</span></span>
<span data-ttu-id="f6ff8-123">모듈 zip 패키지에 대한 URL</span><span class="sxs-lookup"><span data-stu-id="f6ff8-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="f6ff8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ff8-124">-DefaultProfile</span></span>
<span data-ttu-id="f6ff8-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f6ff8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6ff8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f6ff8-126">-Name</span></span>
<span data-ttu-id="f6ff8-127">이 cmdlet에서 가져오는 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="f6ff8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ff8-128">-ResourceGroupName</span></span>
<span data-ttu-id="f6ff8-129">이 cmdlet에서 모듈을 가져오는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="f6ff8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ff8-130">CommonParameters</span></span>
<span data-ttu-id="f6ff8-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ff8-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6ff8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ff8-133">입력</span><span class="sxs-lookup"><span data-stu-id="f6ff8-133">INPUTS</span></span>

### <span data-ttu-id="f6ff8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f6ff8-134">System.String</span></span>

### <span data-ttu-id="f6ff8-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f6ff8-135">System.Uri</span></span>

## <span data-ttu-id="f6ff8-136">출력</span><span class="sxs-lookup"><span data-stu-id="f6ff8-136">OUTPUTS</span></span>

### <span data-ttu-id="f6ff8-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="f6ff8-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f6ff8-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6ff8-138">NOTES</span></span>

## <span data-ttu-id="f6ff8-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6ff8-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6ff8-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f6ff8-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="f6ff8-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f6ff8-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="f6ff8-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f6ff8-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


