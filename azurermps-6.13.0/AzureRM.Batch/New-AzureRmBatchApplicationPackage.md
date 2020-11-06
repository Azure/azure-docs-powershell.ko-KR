---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: bbe3dbc5a929040bfa10efac952b3500529a075d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524580"
---
# <span data-ttu-id="c0439-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0439-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="c0439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0439-102">SYNOPSIS</span></span>
<span data-ttu-id="c0439-103">일괄 처리 계정에 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0439-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0439-104">SYNTAX</span></span>

### <span data-ttu-id="c0439-105">UploadAndActivate (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0439-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0439-106">고만</span><span class="sxs-lookup"><span data-stu-id="c0439-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0439-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0439-107">DESCRIPTION</span></span>
<span data-ttu-id="c0439-108">**새 AzureRmBatchApplicationPackage** Cmdlet은 Azure Batch 계정에서 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="c0439-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0439-109">EXAMPLES</span></span>

### <span data-ttu-id="c0439-110">예제 1: 일괄 처리 계정에 응용 프로그램 패키지 설치</span><span class="sxs-lookup"><span data-stu-id="c0439-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="c0439-111">이 명령은 Litware 응용 프로그램의 버전 1.0를 만들고 활성화 하 고 litware.1.0.zip의 콘텐츠를 응용 프로그램 패키지 콘텐츠로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="c0439-112">변수</span><span class="sxs-lookup"><span data-stu-id="c0439-112">PARAMETERS</span></span>

### <span data-ttu-id="c0439-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0439-113">-AccountName</span></span>
<span data-ttu-id="c0439-114">이 cmdlet이 응용 프로그램 패키지를 추가 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="c0439-115">-고 대만</span><span class="sxs-lookup"><span data-stu-id="c0439-115">-ActivateOnly</span></span>
<span data-ttu-id="c0439-116">이 cmdlet이 이미 업로드 된 응용 프로그램 패키지를 활성화 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0439-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c0439-117">-ApplicationId</span></span>
<span data-ttu-id="c0439-118">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="c0439-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c0439-119">-ApplicationVersion</span></span>
<span data-ttu-id="c0439-120">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0439-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0439-121">-DefaultProfile</span></span>
<span data-ttu-id="c0439-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0439-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c0439-123">-FilePath</span></span>
<span data-ttu-id="c0439-124">업로드할 파일을 응용 프로그램 패키지 이진 파일로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0439-125">-형식</span><span class="sxs-lookup"><span data-stu-id="c0439-125">-Format</span></span>
<span data-ttu-id="c0439-126">응용 프로그램 패키지 이진 파일의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0439-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0439-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0439-128">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c0439-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0439-129">CommonParameters</span></span>
<span data-ttu-id="c0439-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0439-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0439-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0439-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0439-132">입력</span><span class="sxs-lookup"><span data-stu-id="c0439-132">INPUTS</span></span>

### <span data-ttu-id="c0439-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0439-133">System.String</span></span>

### <span data-ttu-id="c0439-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0439-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0439-135">출력</span><span class="sxs-lookup"><span data-stu-id="c0439-135">OUTPUTS</span></span>

### <span data-ttu-id="c0439-136">Microsoft.Azure.Commands.Batch. PSApplicationPackage 모델</span><span class="sxs-lookup"><span data-stu-id="c0439-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="c0439-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c0439-137">NOTES</span></span>

## <span data-ttu-id="c0439-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0439-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0439-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0439-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="c0439-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0439-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c0439-141">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0439-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="c0439-142">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0439-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="c0439-143">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0439-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c0439-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0439-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


