---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009824"
---
# <span data-ttu-id="9115b-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9115b-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="9115b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9115b-102">SYNOPSIS</span></span>
<span data-ttu-id="9115b-103">Automation에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="9115b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9115b-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9115b-105">설명</span><span class="sxs-lookup"><span data-stu-id="9115b-105">DESCRIPTION</span></span>
<span data-ttu-id="9115b-106">**Set-AzAutomationModule** cmdlet은 Azure Automation에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="9115b-107">이 명령은 .zip 파일 이름 확장이 있는 압축된 파일을 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="9115b-108">파일에는 다음 형식 중 하나인 파일이 포함된 폴더가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="9115b-109">.psm1 또는 .dll 파일 이름 확장이 있는 wps_2 모듈</span><span class="sxs-lookup"><span data-stu-id="9115b-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="9115b-110">.psd1 파일 이름 확장명을 wps_2 모듈 매니페스트는 .zip 파일의 이름, 폴더의 이름 및 폴더의 파일 이름이 같아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="9115b-111">.zip 파일을 Automation 서비스가 액세스할 수 있는 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="9115b-112">이 cmdlet 또는 wps_2 cmdlet을 사용하여 automation에 New-AzAutomationModule 모듈을 가져오는 경우 작업은 비동기입니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="9115b-113">명령은 가져오기 성공 여부와 실패 여부를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="9115b-114">성공 여부를 확인한 다음 명령을 `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` 실행합니다. ModuleName이 **ProvisioningState** 속성을 성공한 값으로 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="9115b-115">예제</span><span class="sxs-lookup"><span data-stu-id="9115b-115">EXAMPLES</span></span>

### <span data-ttu-id="9115b-116">예제 1: 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="9115b-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9115b-117">이 명령은 ContosoModule이라는 기존 모듈의 업데이트된 버전을 Contoso17이라는 Automation 계정으로 가져온다.</span><span class="sxs-lookup"><span data-stu-id="9115b-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="9115b-118">모듈은 contosostorage라는 저장소 계정의 Azure Blob 및 모듈이라는 컨테이너에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9115b-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9115b-119">PARAMETERS</span></span>

### <span data-ttu-id="9115b-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9115b-120">-AutomationAccountName</span></span>
<span data-ttu-id="9115b-121">이 cmdlet이 모듈을 업데이트하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="9115b-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9115b-122">-ContentLinkUri</span></span>
<span data-ttu-id="9115b-123">이 cmdlet에서 가져오는 모듈의 새 버전을 포함하는 .zip 파일의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9115b-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="9115b-124">-ContentLinkVersion</span></span>
<span data-ttu-id="9115b-125">이 cmdlet이 Automation을 업데이트하는 모듈 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="9115b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9115b-126">-DefaultProfile</span></span>
<span data-ttu-id="9115b-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9115b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9115b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9115b-128">-Name</span></span>
<span data-ttu-id="9115b-129">이 cmdlet에서 가져오는 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9115b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9115b-130">-ResourceGroupName</span></span>
<span data-ttu-id="9115b-131">이 cmdlet이 모듈을 업데이트하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="9115b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9115b-132">CommonParameters</span></span>
<span data-ttu-id="9115b-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9115b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9115b-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9115b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9115b-135">입력</span><span class="sxs-lookup"><span data-stu-id="9115b-135">INPUTS</span></span>

### <span data-ttu-id="9115b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9115b-136">System.String</span></span>

### <span data-ttu-id="9115b-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="9115b-137">System.Uri</span></span>

## <span data-ttu-id="9115b-138">출력</span><span class="sxs-lookup"><span data-stu-id="9115b-138">OUTPUTS</span></span>

### <span data-ttu-id="9115b-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="9115b-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9115b-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9115b-140">NOTES</span></span>

## <span data-ttu-id="9115b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9115b-141">RELATED LINKS</span></span>

[<span data-ttu-id="9115b-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9115b-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="9115b-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9115b-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="9115b-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9115b-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


