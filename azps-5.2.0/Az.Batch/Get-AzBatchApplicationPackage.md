---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330969"
---
# <span data-ttu-id="2ca76-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ca76-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="2ca76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca76-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca76-103">Batch 계정의 애플리케이션 패키지에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="2ca76-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ca76-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ca76-105">설명</span><span class="sxs-lookup"><span data-stu-id="2ca76-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca76-106">**Get-AzBatchApplicationPackage** cmdlet은 Azure Batch 계정의 애플리케이션 패키지에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="2ca76-107">예제</span><span class="sxs-lookup"><span data-stu-id="2ca76-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca76-108">예제 1: Batch 계정에서 애플리케이션 패키지의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="2ca76-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="2ca76-109">이 명령은 Litware 패키지 버전 1.0의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="2ca76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ca76-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca76-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ca76-111">-AccountName</span></span>
<span data-ttu-id="2ca76-112">이 cmdlet이 정보를 얻을 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="2ca76-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="2ca76-113">-ApplicationName</span></span>
<span data-ttu-id="2ca76-114">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca76-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="2ca76-115">-ApplicationVersion</span></span>
<span data-ttu-id="2ca76-116">애플리케이션의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca76-117">-DefaultProfile</span></span>
<span data-ttu-id="2ca76-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca76-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ca76-120">Batch 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="2ca76-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca76-121">CommonParameters</span></span>
<span data-ttu-id="2ca76-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ca76-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca76-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ca76-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca76-124">입력</span><span class="sxs-lookup"><span data-stu-id="2ca76-124">INPUTS</span></span>

### <span data-ttu-id="2ca76-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2ca76-125">System.String</span></span>

## <span data-ttu-id="2ca76-126">출력</span><span class="sxs-lookup"><span data-stu-id="2ca76-126">OUTPUTS</span></span>

### <span data-ttu-id="2ca76-127">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ca76-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="2ca76-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ca76-128">NOTES</span></span>

## <span data-ttu-id="2ca76-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ca76-129">RELATED LINKS</span></span>

[<span data-ttu-id="2ca76-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ca76-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="2ca76-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ca76-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="2ca76-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ca76-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="2ca76-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ca76-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="2ca76-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2ca76-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="2ca76-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2ca76-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


