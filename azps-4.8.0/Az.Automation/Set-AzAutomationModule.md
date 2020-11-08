---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048513"
---
# <span data-ttu-id="30d3e-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="30d3e-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="30d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="30d3e-103">자동화에서 모듈을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="30d3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30d3e-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30d3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="30d3e-106">**Set-AzAutomationModule** Cmdlet은 Azure Automation의 모듈을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="30d3e-107">이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="30d3e-108">파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="30d3e-109">파일 이름 확장명이 psm1 또는 .dll 인 wps_2 모듈</span><span class="sxs-lookup"><span data-stu-id="30d3e-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="30d3e-110">확장명이 psd1 인 모듈 매니페스트는 .zip 파일 이름, 폴더 이름, 폴더에 있는 파일의 이름 등이 동일 해야 합니다 wps_2.</span><span class="sxs-lookup"><span data-stu-id="30d3e-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="30d3e-111">.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="30d3e-112">이 cmdlet 또는 New-AzAutomationModule cmdlet을 사용 하 여 wps_2 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="30d3e-113">명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="30d3e-114">성공 여부를 확인 하려면 다음 명령을 실행 합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName의 값에 대해 **ProvisioningState** 속성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="30d3e-115">예제의</span><span class="sxs-lookup"><span data-stu-id="30d3e-115">EXAMPLES</span></span>

### <span data-ttu-id="30d3e-116">예제 1: 모듈 업데이트</span><span class="sxs-lookup"><span data-stu-id="30d3e-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30d3e-117">이 명령은 ContosoModule 이라는 기존 모듈의 업데이트 된 버전을 Contoso17 라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="30d3e-118">이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="30d3e-119">변수</span><span class="sxs-lookup"><span data-stu-id="30d3e-119">PARAMETERS</span></span>

### <span data-ttu-id="30d3e-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30d3e-120">-AutomationAccountName</span></span>
<span data-ttu-id="30d3e-121">이 cmdlet이 모듈을 업데이트 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="30d3e-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="30d3e-122">-ContentLinkUri</span></span>
<span data-ttu-id="30d3e-123">이 cmdlet이 가져오는 새 모듈 버전을 포함 하는 .zip 파일의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="30d3e-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="30d3e-124">-ContentLinkVersion</span></span>
<span data-ttu-id="30d3e-125">이 cmdlet이 자동화를 업데이트 하는 모듈의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="30d3e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d3e-126">-DefaultProfile</span></span>
<span data-ttu-id="30d3e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30d3e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30d3e-128">-이름</span><span class="sxs-lookup"><span data-stu-id="30d3e-128">-Name</span></span>
<span data-ttu-id="30d3e-129">이 cmdlet이 가져오는 모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="30d3e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d3e-130">-ResourceGroupName</span></span>
<span data-ttu-id="30d3e-131">이 cmdlet이 모듈을 업데이트 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="30d3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d3e-132">CommonParameters</span></span>
<span data-ttu-id="30d3e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30d3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d3e-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d3e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d3e-135">입력</span><span class="sxs-lookup"><span data-stu-id="30d3e-135">INPUTS</span></span>

### <span data-ttu-id="30d3e-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30d3e-136">System.String</span></span>

### <span data-ttu-id="30d3e-137">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="30d3e-137">System.Uri</span></span>

## <span data-ttu-id="30d3e-138">출력</span><span class="sxs-lookup"><span data-stu-id="30d3e-138">OUTPUTS</span></span>

### <span data-ttu-id="30d3e-139">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="30d3e-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="30d3e-140">상속자</span><span class="sxs-lookup"><span data-stu-id="30d3e-140">NOTES</span></span>

## <span data-ttu-id="30d3e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30d3e-141">RELATED LINKS</span></span>

[<span data-ttu-id="30d3e-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="30d3e-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="30d3e-143">새로운 AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="30d3e-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="30d3e-144">제거-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="30d3e-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


