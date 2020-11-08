---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 65a48a000e5b3e4377ca2518992ad80242f9e4d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034700"
---
# <span data-ttu-id="3fddc-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3fddc-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="3fddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fddc-102">SYNOPSIS</span></span>
<span data-ttu-id="3fddc-103">Azure 저장소 Blob 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="3fddc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fddc-104">SYNTAX</span></span>

### <span data-ttu-id="3fddc-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3fddc-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fddc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3fddc-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fddc-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="3fddc-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fddc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3fddc-108">DESCRIPTION</span></span>
<span data-ttu-id="3fddc-109">**AzStorageBlobServiceProperty** Cmdlet은 Azure 저장소 Blob 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="3fddc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3fddc-110">EXAMPLES</span></span>

### <span data-ttu-id="3fddc-111">예제 1: 지정 된 저장소 계정의 Azure Storage Blob services 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="3fddc-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days 
------------------ ----------------- --------------------- ----------------------------- -------------------------- 
myresourcegroup    mystorageaccount  2018-03-28            False                                                    
```

<span data-ttu-id="3fddc-112">이 명령은 지정 된 저장소 계정의 Blob services 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="3fddc-113">변수</span><span class="sxs-lookup"><span data-stu-id="3fddc-113">PARAMETERS</span></span>

### <span data-ttu-id="3fddc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fddc-114">-DefaultProfile</span></span>
<span data-ttu-id="3fddc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fddc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fddc-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fddc-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fddc-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fddc-118">-ResourceId</span></span>
<span data-ttu-id="3fddc-119">Blob 서비스 속성 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fddc-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-120">-StorageAccount</span></span>
<span data-ttu-id="3fddc-121">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="3fddc-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fddc-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3fddc-122">-StorageAccountName</span></span>
<span data-ttu-id="3fddc-123">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fddc-124">CommonParameters</span></span>
<span data-ttu-id="3fddc-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fddc-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fddc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fddc-127">입력</span><span class="sxs-lookup"><span data-stu-id="3fddc-127">INPUTS</span></span>

### <span data-ttu-id="3fddc-128">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3fddc-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3fddc-129">System.String</span></span>

## <span data-ttu-id="3fddc-130">출력</span><span class="sxs-lookup"><span data-stu-id="3fddc-130">OUTPUTS</span></span>

### <span data-ttu-id="3fddc-131">Microsoft. a. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="3fddc-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="3fddc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3fddc-132">NOTES</span></span>

## <span data-ttu-id="3fddc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fddc-133">RELATED LINKS</span></span>
