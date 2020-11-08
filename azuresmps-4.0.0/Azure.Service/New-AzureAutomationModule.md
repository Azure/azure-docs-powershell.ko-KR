---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046223"
---
# <span data-ttu-id="6f81e-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f81e-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="6f81e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f81e-102">SYNOPSIS</span></span>

<span data-ttu-id="6f81e-103">모듈을 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="6f81e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f81e-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f81e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f81e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6f81e-106">**새-AzureAutomationModule** cmdlet은 모듈을 Azure 자동화로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="6f81e-107">모듈은 .zip 확장명을 가진 압축 파일로, 다음 파일 형식 중 하나를 포함 하는 폴더를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="6f81e-108">Windows PowerShell 모듈 (psm1 파일)</span><span class="sxs-lookup"><span data-stu-id="6f81e-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="6f81e-109">Windows PowerShell 모듈 매니페스트 (psd1 파일)</span><span class="sxs-lookup"><span data-stu-id="6f81e-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="6f81e-110">어셈블리 (dll 파일)입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-110">An assembly (dll file).</span></span>

<span data-ttu-id="6f81e-111">Zip 파일의 이름, zip 파일의 폴더 및 폴더 (psm1, psd. 1 또는 .dll)의 파일이 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="6f81e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6f81e-112">EXAMPLES</span></span>

### <span data-ttu-id="6f81e-113">예제 1: 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="6f81e-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="6f81e-114">이 명령은 ContosoModule 이라는 모듈을 Contoso17 이라는 Automation 계정으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="6f81e-115">이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="6f81e-116">변수</span><span class="sxs-lookup"><span data-stu-id="6f81e-116">PARAMETERS</span></span>

### <span data-ttu-id="6f81e-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f81e-117">-AutomationAccountName</span></span>
<span data-ttu-id="6f81e-118">모듈이 저장 될 자동화 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81e-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="6f81e-119">-ContentLink</span></span>
<span data-ttu-id="6f81e-120">모듈 파일에 대 한 경로를 지정 하는 웹 사이트 또는 Azure blob 저장소와 같은 공개 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="6f81e-121">이 위치는 publically 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6f81e-122">-Name</span></span>
<span data-ttu-id="6f81e-123">모듈의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81e-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="6f81e-124">-Profile</span></span>
<span data-ttu-id="6f81e-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f81e-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81e-127">태그</span><span class="sxs-lookup"><span data-stu-id="6f81e-127">-Tags</span></span>
<span data-ttu-id="6f81e-128">모듈과 관련 된 하나 이상의 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f81e-129">CommonParameters</span></span>
<span data-ttu-id="6f81e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f81e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f81e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f81e-132">입력</span><span class="sxs-lookup"><span data-stu-id="6f81e-132">INPUTS</span></span>

## <span data-ttu-id="6f81e-133">출력</span><span class="sxs-lookup"><span data-stu-id="6f81e-133">OUTPUTS</span></span>

### <span data-ttu-id="6f81e-134">Microsoft Azure. 모듈별. 모듈</span><span class="sxs-lookup"><span data-stu-id="6f81e-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="6f81e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6f81e-135">NOTES</span></span>

## <span data-ttu-id="6f81e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f81e-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f81e-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f81e-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="6f81e-138">-AzureAutomationModule 제거</span><span class="sxs-lookup"><span data-stu-id="6f81e-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="6f81e-139">Set AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f81e-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


