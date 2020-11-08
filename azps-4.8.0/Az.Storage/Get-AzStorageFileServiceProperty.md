---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213809"
---
# <span data-ttu-id="27a18-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27a18-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="27a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a18-102">SYNOPSIS</span></span>
<span data-ttu-id="27a18-103">Azure 저장소 파일 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="27a18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27a18-104">SYNTAX</span></span>

### <span data-ttu-id="27a18-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="27a18-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a18-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="27a18-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27a18-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="27a18-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27a18-108">설명은</span><span class="sxs-lookup"><span data-stu-id="27a18-108">DESCRIPTION</span></span>
<span data-ttu-id="27a18-109">**AzStorageFileServiceProperty** Cmdlet은 Azure 저장소 파일 서비스에 대 한 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="27a18-110">예제의</span><span class="sxs-lookup"><span data-stu-id="27a18-110">EXAMPLES</span></span>

### <span data-ttu-id="27a18-111">예제 1: 지정 된 저장소 계정의 Azure 저장소 파일 서비스 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="27a18-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="27a18-112">이 명령은 지정 된 저장소 계정의 파일 서비스 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="27a18-113">변수</span><span class="sxs-lookup"><span data-stu-id="27a18-113">PARAMETERS</span></span>

### <span data-ttu-id="27a18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a18-114">-DefaultProfile</span></span>
<span data-ttu-id="27a18-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a18-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a18-116">-ResourceGroupName</span></span>
<span data-ttu-id="27a18-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="27a18-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27a18-118">-ResourceId</span></span>
<span data-ttu-id="27a18-119">저장소 계정 리소스 Id 또는 파일 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="27a18-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="27a18-120">-StorageAccount</span></span>
<span data-ttu-id="27a18-121">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="27a18-121">Storage account object</span></span>

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

### <span data-ttu-id="27a18-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27a18-122">-StorageAccountName</span></span>
<span data-ttu-id="27a18-123">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="27a18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a18-124">CommonParameters</span></span>
<span data-ttu-id="27a18-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a18-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a18-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a18-127">입력</span><span class="sxs-lookup"><span data-stu-id="27a18-127">INPUTS</span></span>

### <span data-ttu-id="27a18-128">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27a18-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="27a18-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27a18-129">System.String</span></span>

## <span data-ttu-id="27a18-130">출력</span><span class="sxs-lookup"><span data-stu-id="27a18-130">OUTPUTS</span></span>

### <span data-ttu-id="27a18-131">PSFileServiceProperties를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a18-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="27a18-132">상속자</span><span class="sxs-lookup"><span data-stu-id="27a18-132">NOTES</span></span>

## <span data-ttu-id="27a18-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27a18-133">RELATED LINKS</span></span>
