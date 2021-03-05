---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 9503f62667405c8e7a652bffc150a747eadb40f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981488"
---
# <span data-ttu-id="b1539-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b1539-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="b1539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1539-102">SYNOPSIS</span></span>
<span data-ttu-id="b1539-103">Azure Storage 파일 서비스에 대한 서비스 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="b1539-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1539-104">SYNTAX</span></span>

### <span data-ttu-id="b1539-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1539-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1539-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b1539-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1539-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b1539-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1539-108">설명</span><span class="sxs-lookup"><span data-stu-id="b1539-108">DESCRIPTION</span></span>
<span data-ttu-id="b1539-109">**Get-AzStorageFileServiceProperty** cmdlet은 Azure Storage 파일 서비스에 대한 서비스 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="b1539-110">예제</span><span class="sxs-lookup"><span data-stu-id="b1539-110">EXAMPLES</span></span>

### <span data-ttu-id="b1539-111">예제 1: 지정된 Storage 계정의 Azure Storage 파일 서비스 속성 다운로드</span><span class="sxs-lookup"><span data-stu-id="b1539-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 3
```

<span data-ttu-id="b1539-112">이 명령은 지정된 Storage 계정의 File services 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="b1539-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b1539-113">PARAMETERS</span></span>

### <span data-ttu-id="b1539-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1539-114">-DefaultProfile</span></span>
<span data-ttu-id="b1539-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1539-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1539-116">-ResourceGroupName</span></span>
<span data-ttu-id="b1539-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1539-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1539-118">-ResourceId</span></span>
<span data-ttu-id="b1539-119">Storage 계정 리소스 ID 또는 파일 서비스 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1539-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1539-120">-StorageAccount</span></span>
<span data-ttu-id="b1539-121">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="b1539-121">Storage account object</span></span>

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

### <span data-ttu-id="b1539-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1539-122">-StorageAccountName</span></span>
<span data-ttu-id="b1539-123">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="b1539-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1539-124">CommonParameters</span></span>
<span data-ttu-id="b1539-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1539-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1539-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b1539-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1539-127">입력</span><span class="sxs-lookup"><span data-stu-id="b1539-127">INPUTS</span></span>

### <span data-ttu-id="b1539-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1539-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b1539-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b1539-129">System.String</span></span>

## <span data-ttu-id="b1539-130">출력</span><span class="sxs-lookup"><span data-stu-id="b1539-130">OUTPUTS</span></span>

### <span data-ttu-id="b1539-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b1539-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="b1539-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1539-132">NOTES</span></span>

## <span data-ttu-id="b1539-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1539-133">RELATED LINKS</span></span>
