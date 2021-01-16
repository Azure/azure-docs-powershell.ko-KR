---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369223"
---
# <span data-ttu-id="6812a-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6812a-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="6812a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6812a-102">SYNOPSIS</span></span>
<span data-ttu-id="6812a-103">Azure Storage 서비스에 대한 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6812a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6812a-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6812a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6812a-105">DESCRIPTION</span></span>
<span data-ttu-id="6812a-106">**Update-AzStorageServiceProperty** cmdlet은 Azure Storage 서비스에 대한 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6812a-107">예제</span><span class="sxs-lookup"><span data-stu-id="6812a-107">EXAMPLES</span></span>

### <span data-ttu-id="6812a-108">예제 1: Blob Service DefaultServiceVersion을 2017-04-17로 설정</span><span class="sxs-lookup"><span data-stu-id="6812a-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="6812a-109">이 명령은 Blob Service의 DefaultServiceVersion을 2017-04-17로 설정</span><span class="sxs-lookup"><span data-stu-id="6812a-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="6812a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6812a-110">PARAMETERS</span></span>

### <span data-ttu-id="6812a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6812a-111">-Context</span></span>
<span data-ttu-id="6812a-112">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6812a-113">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6812a-114">-DefaultProfile</span></span>
<span data-ttu-id="6812a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="6812a-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="6812a-117">DefaultServiceVersion은 들어오는 요청의 버전이 지정되지 않은 경우 Blob service에 대한 요청에 사용할 기본 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="6812a-118">가능한 값에는 버전 2008-10-27 및 모든 최신 버전이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="6812a-119">자세한 내용은 https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="6812a-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6812a-120">-PassThru</span></span>
<span data-ttu-id="6812a-121">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="6812a-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6812a-122">-ServiceType</span></span>
<span data-ttu-id="6812a-123">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-123">Specifies the storage service type.</span></span>
<span data-ttu-id="6812a-124">이 cmdlet은 이 매개 변수가 지정하는 서비스 형식에 대한 로깅 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6812a-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="6812a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6812a-126">Blob</span><span class="sxs-lookup"><span data-stu-id="6812a-126">Blob</span></span> 
- <span data-ttu-id="6812a-127">표</span><span class="sxs-lookup"><span data-stu-id="6812a-127">Table</span></span>
- <span data-ttu-id="6812a-128">큐</span><span class="sxs-lookup"><span data-stu-id="6812a-128">Queue</span></span>
- <span data-ttu-id="6812a-129">파일</span><span class="sxs-lookup"><span data-stu-id="6812a-129">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6812a-130">-Confirm</span></span>
<span data-ttu-id="6812a-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6812a-132">-WhatIf</span></span>
<span data-ttu-id="6812a-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6812a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6812a-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6812a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6812a-135">CommonParameters</span></span>
<span data-ttu-id="6812a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6812a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6812a-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6812a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6812a-138">입력</span><span class="sxs-lookup"><span data-stu-id="6812a-138">INPUTS</span></span>

### <span data-ttu-id="6812a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6812a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6812a-140">출력</span><span class="sxs-lookup"><span data-stu-id="6812a-140">OUTPUTS</span></span>

### <span data-ttu-id="6812a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="6812a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="6812a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6812a-142">NOTES</span></span>

## <span data-ttu-id="6812a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6812a-143">RELATED LINKS</span></span>