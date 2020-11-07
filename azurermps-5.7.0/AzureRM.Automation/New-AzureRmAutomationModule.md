---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702176"
---
# <span data-ttu-id="4aafb-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4aafb-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="4aafb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aafb-102">SYNOPSIS</span></span>
<span data-ttu-id="4aafb-103">모듈을 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aafb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aafb-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aafb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4aafb-105">DESCRIPTION</span></span>
<span data-ttu-id="4aafb-106">**새 AzureRmAutomationModule** cmdlet은 모듈을 Azure 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="4aafb-107">이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="4aafb-108">파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="4aafb-109">파일 이름 확장명이 psm1 또는 .dll 인 wps_2 모듈</span><span class="sxs-lookup"><span data-stu-id="4aafb-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="4aafb-110">psd1 파일 이름 확장명을 가진 wps_2 모듈 매니페스트</span><span class="sxs-lookup"><span data-stu-id="4aafb-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="4aafb-111">.Zip 파일의 이름과 폴더의 이름 및 폴더에 있는 파일의 이름이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="4aafb-112">.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="4aafb-113">이 cmdlet 또는 Set-AzureRmAutomationModule cmdlet을 사용 하 여 wps_2 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="4aafb-114">명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="4aafb-115">성공 여부를 확인 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="4aafb-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `모듈</span><span class="sxs-lookup"><span data-stu-id="4aafb-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="4aafb-117">**ProvisioningState** 속성에 성공 값이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="4aafb-118">예제의</span><span class="sxs-lookup"><span data-stu-id="4aafb-118">EXAMPLES</span></span>

### <span data-ttu-id="4aafb-119">예제 1: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="4aafb-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4aafb-120">이 명령은 ContosoModule 이라는 모듈을 Contoso17 이라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="4aafb-121">이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="4aafb-122">변수</span><span class="sxs-lookup"><span data-stu-id="4aafb-122">PARAMETERS</span></span>

### <span data-ttu-id="4aafb-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4aafb-123">-AutomationAccountName</span></span>
<span data-ttu-id="4aafb-124">이 cmdlet이 모듈을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafb-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="4aafb-125">-ContentLinkUri</span></span>
<span data-ttu-id="4aafb-126">모듈 zip 패키지에 대 한 url입니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-126">The url to a module zip package</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aafb-127">-DefaultProfile</span></span>
<span data-ttu-id="4aafb-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4aafb-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aafb-129">-이름</span><span class="sxs-lookup"><span data-stu-id="4aafb-129">-Name</span></span>
<span data-ttu-id="4aafb-130">이 cmdlet이 가져오는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-130">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aafb-131">-ResourceGroupName</span></span>
<span data-ttu-id="4aafb-132">이 cmdlet가 모듈을 가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-132">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aafb-133">CommonParameters</span></span>
<span data-ttu-id="4aafb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aafb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aafb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aafb-136">입력</span><span class="sxs-lookup"><span data-stu-id="4aafb-136">INPUTS</span></span>

### <span data-ttu-id="4aafb-137">않아야</span><span class="sxs-lookup"><span data-stu-id="4aafb-137">None</span></span>
<span data-ttu-id="4aafb-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aafb-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aafb-139">출력</span><span class="sxs-lookup"><span data-stu-id="4aafb-139">OUTPUTS</span></span>

### <span data-ttu-id="4aafb-140">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="4aafb-140">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4aafb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4aafb-141">NOTES</span></span>

## <span data-ttu-id="4aafb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aafb-142">RELATED LINKS</span></span>

[<span data-ttu-id="4aafb-143">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4aafb-143">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="4aafb-144">제거-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4aafb-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="4aafb-145">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4aafb-145">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


