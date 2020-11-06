---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 0e1182843ee57809fe3c6a0ed1c7f516678fc1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529849"
---
# <span data-ttu-id="031b1-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="031b1-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="031b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="031b1-102">SYNOPSIS</span></span>
<span data-ttu-id="031b1-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="031b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="031b1-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="031b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="031b1-105">DESCRIPTION</span></span>
<span data-ttu-id="031b1-106">**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)에 있는 항목 (ACE)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="031b1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="031b1-107">EXAMPLES</span></span>

### <span data-ttu-id="031b1-108">예제 1: 폴더에 대 한 ACL 가져오기</span><span class="sxs-lookup"><span data-stu-id="031b1-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="031b1-109">이 명령은 지정 된 Data Lake Store 계정의 루트 디렉터리에 대 한 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="031b1-110">변수</span><span class="sxs-lookup"><span data-stu-id="031b1-110">PARAMETERS</span></span>

### <span data-ttu-id="031b1-111">-계정</span><span class="sxs-lookup"><span data-stu-id="031b1-111">-Account</span></span>
<span data-ttu-id="031b1-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031b1-113">-DefaultProfile</span></span>
<span data-ttu-id="031b1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="031b1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="031b1-115">-Path</span></span>
<span data-ttu-id="031b1-116">이 cmdlet에서 ACE를 가져오는 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031b1-117">CommonParameters</span></span>
<span data-ttu-id="031b1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031b1-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031b1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031b1-120">입력</span><span class="sxs-lookup"><span data-stu-id="031b1-120">INPUTS</span></span>

### <span data-ttu-id="031b1-121">않아야</span><span class="sxs-lookup"><span data-stu-id="031b1-121">None</span></span>
<span data-ttu-id="031b1-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="031b1-123">출력</span><span class="sxs-lookup"><span data-stu-id="031b1-123">OUTPUTS</span></span>

### <span data-ttu-id="031b1-124">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="031b1-124">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="031b1-125">지정 된 폴더 또는 파일에 대 한 ACL 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="031b1-125">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="031b1-126">상속자</span><span class="sxs-lookup"><span data-stu-id="031b1-126">NOTES</span></span>

## <span data-ttu-id="031b1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="031b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="031b1-128">제거-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="031b1-128">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="031b1-129">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="031b1-129">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


