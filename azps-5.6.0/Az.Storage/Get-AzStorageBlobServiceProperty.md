---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 72e26a8fbb059db78fcdfa56721bed94e388ef55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002667"
---
# <span data-ttu-id="68fb4-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="68fb4-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="68fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="68fb4-103">Azure Storage Blob 서비스에 대한 서비스 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="68fb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="68fb4-104">SYNTAX</span></span>

### <span data-ttu-id="68fb4-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="68fb4-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68fb4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="68fb4-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68fb4-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="68fb4-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68fb4-108">설명</span><span class="sxs-lookup"><span data-stu-id="68fb4-108">DESCRIPTION</span></span>
<span data-ttu-id="68fb4-109">**Get-AzStorageBlobServiceProperty** cmdlet은 Azure Storage Blob 서비스에 대한 서비스 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="68fb4-110">예제</span><span class="sxs-lookup"><span data-stu-id="68fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="68fb4-111">예제 1: 지정된 Storage 계정의 Azure Storage Blob 서비스 속성 사용</span><span class="sxs-lookup"><span data-stu-id="68fb4-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
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

<span data-ttu-id="68fb4-112">이 명령은 지정된 Storage 계정의 Blob 서비스 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="68fb4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68fb4-113">PARAMETERS</span></span>

### <span data-ttu-id="68fb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fb4-114">-DefaultProfile</span></span>
<span data-ttu-id="68fb4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68fb4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fb4-116">-ResourceGroupName</span></span>
<span data-ttu-id="68fb4-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="68fb4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68fb4-118">-ResourceId</span></span>
<span data-ttu-id="68fb4-119">Blob Service 속성 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="68fb4-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="68fb4-120">-StorageAccount</span></span>
<span data-ttu-id="68fb4-121">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="68fb4-121">Storage account object</span></span>

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

### <span data-ttu-id="68fb4-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68fb4-122">-StorageAccountName</span></span>
<span data-ttu-id="68fb4-123">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="68fb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fb4-124">CommonParameters</span></span>
<span data-ttu-id="68fb4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68fb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fb4-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="68fb4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fb4-127">입력</span><span class="sxs-lookup"><span data-stu-id="68fb4-127">INPUTS</span></span>

### <span data-ttu-id="68fb4-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68fb4-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="68fb4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="68fb4-129">System.String</span></span>

## <span data-ttu-id="68fb4-130">출력</span><span class="sxs-lookup"><span data-stu-id="68fb4-130">OUTPUTS</span></span>

### <span data-ttu-id="68fb4-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="68fb4-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="68fb4-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68fb4-132">NOTES</span></span>

## <span data-ttu-id="68fb4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68fb4-133">RELATED LINKS</span></span>
