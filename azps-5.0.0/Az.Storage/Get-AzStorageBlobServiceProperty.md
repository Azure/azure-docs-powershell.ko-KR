---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226107"
---
# <span data-ttu-id="13a29-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="13a29-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="13a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a29-102">SYNOPSIS</span></span>
<span data-ttu-id="13a29-103">Azure 저장소 Blob 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="13a29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13a29-104">SYNTAX</span></span>

### <span data-ttu-id="13a29-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="13a29-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13a29-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="13a29-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13a29-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="13a29-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13a29-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13a29-108">DESCRIPTION</span></span>
<span data-ttu-id="13a29-109">**AzStorageBlobServiceProperty** Cmdlet은 Azure 저장소 Blob 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="13a29-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13a29-110">EXAMPLES</span></span>

### <span data-ttu-id="13a29-111">예제 1: 지정 된 저장소 계정의 Azure Storage Blob services 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="13a29-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="13a29-112">이 명령은 지정 된 저장소 계정의 Blob services 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="13a29-113">변수</span><span class="sxs-lookup"><span data-stu-id="13a29-113">PARAMETERS</span></span>

### <span data-ttu-id="13a29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a29-114">-DefaultProfile</span></span>
<span data-ttu-id="13a29-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a29-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a29-116">-ResourceGroupName</span></span>
<span data-ttu-id="13a29-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="13a29-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13a29-118">-ResourceId</span></span>
<span data-ttu-id="13a29-119">Blob 서비스 속성 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="13a29-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="13a29-120">-StorageAccount</span></span>
<span data-ttu-id="13a29-121">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="13a29-121">Storage account object</span></span>

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

### <span data-ttu-id="13a29-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="13a29-122">-StorageAccountName</span></span>
<span data-ttu-id="13a29-123">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="13a29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a29-124">CommonParameters</span></span>
<span data-ttu-id="13a29-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a29-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a29-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a29-127">입력</span><span class="sxs-lookup"><span data-stu-id="13a29-127">INPUTS</span></span>

### <span data-ttu-id="13a29-128">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13a29-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="13a29-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13a29-129">System.String</span></span>

## <span data-ttu-id="13a29-130">출력</span><span class="sxs-lookup"><span data-stu-id="13a29-130">OUTPUTS</span></span>

### <span data-ttu-id="13a29-131">Microsoft. a. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="13a29-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="13a29-132">상속자</span><span class="sxs-lookup"><span data-stu-id="13a29-132">NOTES</span></span>

## <span data-ttu-id="13a29-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13a29-133">RELATED LINKS</span></span>
