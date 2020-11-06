---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: 7bec79c2c2c4bdc794b1d3b260cad53d82fa5d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535332"
---
# <span data-ttu-id="9e9d5-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9e9d5-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="9e9d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9d5-103">자동화에서 모듈을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e9d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e9d5-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9d5-106">**Set-AzureRmAutomationModule** Cmdlet은 Azure Automation의 모듈을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="9e9d5-107">이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="9e9d5-108">파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="9e9d5-109">파일 이름 확장명이 psm1 또는 .dll 인 wps_2 모듈</span><span class="sxs-lookup"><span data-stu-id="9e9d5-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="9e9d5-110">psd1 파일 이름 확장명을 가진 wps_2 모듈 매니페스트</span><span class="sxs-lookup"><span data-stu-id="9e9d5-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="9e9d5-111">.Zip 파일의 이름과 폴더의 이름 및 폴더에 있는 파일의 이름이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="9e9d5-112">.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="9e9d5-113">이 cmdlet 또는 New-AzureRmAutomationModule cmdlet을 사용 하 여 wps_2 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="9e9d5-114">명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="9e9d5-115">성공 여부를 확인 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="9e9d5-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `모듈</span><span class="sxs-lookup"><span data-stu-id="9e9d5-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="9e9d5-117">**ProvisioningState** 속성에 성공 값이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="9e9d5-118">예제의</span><span class="sxs-lookup"><span data-stu-id="9e9d5-118">EXAMPLES</span></span>

### <span data-ttu-id="9e9d5-119">예제 1: 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e9d5-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e9d5-120">이 명령은 ContosoModule 이라는 기존 모듈의 업데이트 된 버전을 Contoso17 라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="9e9d5-121">이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9e9d5-122">변수</span><span class="sxs-lookup"><span data-stu-id="9e9d5-122">PARAMETERS</span></span>

### <span data-ttu-id="9e9d5-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e9d5-123">-AutomationAccountName</span></span>
<span data-ttu-id="9e9d5-124">이 cmdlet이 모듈을 업데이트 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-124">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="9e9d5-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9e9d5-125">-ContentLinkUri</span></span>
<span data-ttu-id="9e9d5-126">이 cmdlet이 가져오는 새 모듈 버전을 포함 하는 .zip 파일의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-126">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9d5-127">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="9e9d5-127">-ContentLinkVersion</span></span>
<span data-ttu-id="9e9d5-128">이 cmdlet이 자동화를 업데이트 하는 모듈의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-128">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9d5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9d5-129">-DefaultProfile</span></span>
<span data-ttu-id="9e9d5-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e9d5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e9d5-131">-이름</span><span class="sxs-lookup"><span data-stu-id="9e9d5-131">-Name</span></span>
<span data-ttu-id="9e9d5-132">이 cmdlet이 가져오는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-132">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9e9d5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9d5-133">-ResourceGroupName</span></span>
<span data-ttu-id="9e9d5-134">이 cmdlet이 모듈을 업데이트 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-134">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="9e9d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9d5-135">CommonParameters</span></span>
<span data-ttu-id="9e9d5-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9d5-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9d5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9d5-138">입력</span><span class="sxs-lookup"><span data-stu-id="9e9d5-138">INPUTS</span></span>

### <span data-ttu-id="9e9d5-139">않아야</span><span class="sxs-lookup"><span data-stu-id="9e9d5-139">None</span></span>
<span data-ttu-id="9e9d5-140">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e9d5-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e9d5-141">출력</span><span class="sxs-lookup"><span data-stu-id="9e9d5-141">OUTPUTS</span></span>

### <span data-ttu-id="9e9d5-142">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="9e9d5-142">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9e9d5-143">상속자</span><span class="sxs-lookup"><span data-stu-id="9e9d5-143">NOTES</span></span>

## <span data-ttu-id="9e9d5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e9d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="9e9d5-145">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9e9d5-145">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="9e9d5-146">새로운 AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9e9d5-146">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="9e9d5-147">제거-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9e9d5-147">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


