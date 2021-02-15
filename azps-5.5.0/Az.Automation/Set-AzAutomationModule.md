---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182137"
---
# <span data-ttu-id="4fee6-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4fee6-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="4fee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fee6-102">SYNOPSIS</span></span>
<span data-ttu-id="4fee6-103">Automation에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="4fee6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fee6-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fee6-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fee6-105">DESCRIPTION</span></span>
<span data-ttu-id="4fee6-106">**Set-AzAutomationModule** cmdlet은 Azure Automation에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="4fee6-107">이 명령은 .zip 파일 이름 확장명을 사용하는 압축 파일을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="4fee6-108">파일에는 다음 형식 중 하나인 파일이 포함된 폴더가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="4fee6-109">wps_2 .psm1 또는 .dll 파일 이름 확장명이 있는 모듈</span><span class="sxs-lookup"><span data-stu-id="4fee6-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="4fee6-110">wps_2 .psd1 파일 이름 확장명을 품은 모듈 매니페스트는 .zip 파일의 이름, 폴더의 이름 및 폴더의 파일 이름이 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="4fee6-111">.zip 파일을 Automation 서비스에서 액세스할 수 있는 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="4fee6-112">이 cmdlet 또는 wps_2 cmdlet을 사용하여 Automation에 New-AzAutomationModule 모듈을 가져오는 경우 작업은 비동기적입니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="4fee6-113">이 명령은 가져오기 성공 또는 실패 여부를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="4fee6-114">성공 여부를 확인하기 위해 다음 명령을 실행합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName은 **ProvisioningState** 속성에서 Succeeded 값을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="4fee6-115">예제</span><span class="sxs-lookup"><span data-stu-id="4fee6-115">EXAMPLES</span></span>

### <span data-ttu-id="4fee6-116">예제 1: 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="4fee6-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4fee6-117">이 명령은 ContosoModule이라는 기존 모듈의 업데이트된 버전을 Contoso17이라는 Automation 계정으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="4fee6-118">모듈은 contosostorage라는 스토리지 계정 및 모듈이라는 컨테이너의 Azure Blob에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="4fee6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fee6-119">PARAMETERS</span></span>

### <span data-ttu-id="4fee6-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4fee6-120">-AutomationAccountName</span></span>
<span data-ttu-id="4fee6-121">이 cmdlet이 모듈을 업데이트하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="4fee6-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="4fee6-122">-ContentLinkUri</span></span>
<span data-ttu-id="4fee6-123">이 cmdlet에서 가져오는 모듈의 새 버전을 포함하는 .zip 파일의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fee6-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="4fee6-124">-ContentLinkVersion</span></span>
<span data-ttu-id="4fee6-125">이 cmdlet이 Automation을 업데이트하는 모듈의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="4fee6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fee6-126">-DefaultProfile</span></span>
<span data-ttu-id="4fee6-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4fee6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fee6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4fee6-128">-Name</span></span>
<span data-ttu-id="4fee6-129">이 cmdlet에서 가져오는 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="4fee6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fee6-130">-ResourceGroupName</span></span>
<span data-ttu-id="4fee6-131">이 cmdlet이 모듈을 업데이트하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="4fee6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fee6-132">CommonParameters</span></span>
<span data-ttu-id="4fee6-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fee6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fee6-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fee6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fee6-135">입력</span><span class="sxs-lookup"><span data-stu-id="4fee6-135">INPUTS</span></span>

### <span data-ttu-id="4fee6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4fee6-136">System.String</span></span>

### <span data-ttu-id="4fee6-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="4fee6-137">System.Uri</span></span>

## <span data-ttu-id="4fee6-138">출력</span><span class="sxs-lookup"><span data-stu-id="4fee6-138">OUTPUTS</span></span>

### <span data-ttu-id="4fee6-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="4fee6-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4fee6-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fee6-140">NOTES</span></span>

## <span data-ttu-id="4fee6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fee6-141">RELATED LINKS</span></span>

[<span data-ttu-id="4fee6-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4fee6-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="4fee6-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4fee6-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="4fee6-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4fee6-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


