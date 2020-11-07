---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: fc1cbddd59d52816b0f7ef3bd664405a98ead518
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876293"
---
# <span data-ttu-id="058a2-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="058a2-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="058a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="058a2-102">SYNOPSIS</span></span>
<span data-ttu-id="058a2-103">Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="058a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="058a2-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="058a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="058a2-105">DESCRIPTION</span></span>
<span data-ttu-id="058a2-106">**AzStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="058a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="058a2-107">EXAMPLES</span></span>

### <span data-ttu-id="058a2-108">예제 1: Blob 서비스에 대 한 로깅 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="058a2-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="058a2-109">이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="058a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="058a2-110">PARAMETERS</span></span>

### <span data-ttu-id="058a2-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="058a2-111">-Context</span></span>
<span data-ttu-id="058a2-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="058a2-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="058a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058a2-114">-DefaultProfile</span></span>
<span data-ttu-id="058a2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058a2-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="058a2-116">-ServiceType</span></span>
<span data-ttu-id="058a2-117">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-117">Specifies the storage service type.</span></span>
<span data-ttu-id="058a2-118">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="058a2-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="058a2-120">블</span><span class="sxs-lookup"><span data-stu-id="058a2-120">Blob</span></span> 
- <span data-ttu-id="058a2-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="058a2-121">Table</span></span>
- <span data-ttu-id="058a2-122">전담팀</span><span class="sxs-lookup"><span data-stu-id="058a2-122">Queue</span></span>
- <span data-ttu-id="058a2-123">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="058a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058a2-124">CommonParameters</span></span>
<span data-ttu-id="058a2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="058a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058a2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="058a2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058a2-127">입력</span><span class="sxs-lookup"><span data-stu-id="058a2-127">INPUTS</span></span>

### <span data-ttu-id="058a2-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="058a2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="058a2-129">출력</span><span class="sxs-lookup"><span data-stu-id="058a2-129">OUTPUTS</span></span>

### <span data-ttu-id="058a2-130">LoggingProperties/. m a w.</span><span class="sxs-lookup"><span data-stu-id="058a2-130">Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="058a2-131">상속자</span><span class="sxs-lookup"><span data-stu-id="058a2-131">NOTES</span></span>

## <span data-ttu-id="058a2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="058a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="058a2-133">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="058a2-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="058a2-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="058a2-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


