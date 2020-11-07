---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697704"
---
# <span data-ttu-id="63274-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63274-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="63274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63274-102">SYNOPSIS</span></span>
<span data-ttu-id="63274-103">일괄 계정에서 응용 프로그램 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63274-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="63274-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63274-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63274-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63274-105">DESCRIPTION</span></span>
<span data-ttu-id="63274-106">**AzBatchApplicationPackage** Cmdlet은 Azure Batch 계정에서 응용 프로그램 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63274-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="63274-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63274-107">EXAMPLES</span></span>

### <span data-ttu-id="63274-108">예제 1: 일괄 처리 계정에서 응용 프로그램 패키지에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="63274-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="63274-109">이 명령은 Litware 패키지의 버전 1.0에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63274-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="63274-110">변수</span><span class="sxs-lookup"><span data-stu-id="63274-110">PARAMETERS</span></span>

### <span data-ttu-id="63274-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63274-111">-AccountName</span></span>
<span data-ttu-id="63274-112">이 cmdlet에서 정보를 가져오는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63274-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="63274-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="63274-113">-ApplicationId</span></span>
<span data-ttu-id="63274-114">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63274-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="63274-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="63274-115">-ApplicationVersion</span></span>
<span data-ttu-id="63274-116">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63274-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="63274-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63274-117">-DefaultProfile</span></span>
<span data-ttu-id="63274-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63274-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63274-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63274-119">-ResourceGroupName</span></span>
<span data-ttu-id="63274-120">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63274-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="63274-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63274-121">CommonParameters</span></span>
<span data-ttu-id="63274-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63274-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63274-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63274-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63274-124">입력</span><span class="sxs-lookup"><span data-stu-id="63274-124">INPUTS</span></span>

### <span data-ttu-id="63274-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63274-125">System.String</span></span>

## <span data-ttu-id="63274-126">출력</span><span class="sxs-lookup"><span data-stu-id="63274-126">OUTPUTS</span></span>

### <span data-ttu-id="63274-127">Microsoft.Azure.Commands.Batch. PSApplicationPackage 모델</span><span class="sxs-lookup"><span data-stu-id="63274-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="63274-128">상속자</span><span class="sxs-lookup"><span data-stu-id="63274-128">NOTES</span></span>

## <span data-ttu-id="63274-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63274-129">RELATED LINKS</span></span>

[<span data-ttu-id="63274-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63274-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="63274-131">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63274-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="63274-132">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63274-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="63274-133">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63274-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="63274-134">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="63274-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="63274-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="63274-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


