---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703753"
---
# <span data-ttu-id="1bc98-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bc98-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="1bc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bc98-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc98-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bc98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bc98-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bc98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1bc98-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc98-106">**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)에 있는 항목 (ACE)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1bc98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1bc98-107">EXAMPLES</span></span>

### <span data-ttu-id="1bc98-108">예제 1: 폴더에 대 한 ACL 가져오기</span><span class="sxs-lookup"><span data-stu-id="1bc98-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="1bc98-109">이 명령은 지정 된 Data Lake Store 계정의 루트 디렉터리에 대 한 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="1bc98-110">변수</span><span class="sxs-lookup"><span data-stu-id="1bc98-110">PARAMETERS</span></span>

### <span data-ttu-id="1bc98-111">-계정</span><span class="sxs-lookup"><span data-stu-id="1bc98-111">-Account</span></span>
<span data-ttu-id="1bc98-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc98-113">-Path</span><span class="sxs-lookup"><span data-stu-id="1bc98-113">-Path</span></span>
<span data-ttu-id="1bc98-114">이 cmdlet에서 ACE를 가져오는 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc98-115">-DefaultProfile</span></span>
<span data-ttu-id="1bc98-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bc98-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc98-117">CommonParameters</span></span>
<span data-ttu-id="1bc98-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc98-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc98-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc98-120">입력</span><span class="sxs-lookup"><span data-stu-id="1bc98-120">INPUTS</span></span>

## <span data-ttu-id="1bc98-121">출력</span><span class="sxs-lookup"><span data-stu-id="1bc98-121">OUTPUTS</span></span>

### <span data-ttu-id="1bc98-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="1bc98-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="1bc98-123">지정 된 폴더 또는 파일에 대 한 ACL 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc98-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="1bc98-124">상속자</span><span class="sxs-lookup"><span data-stu-id="1bc98-124">NOTES</span></span>

## <span data-ttu-id="1bc98-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bc98-125">RELATED LINKS</span></span>

[<span data-ttu-id="1bc98-126">제거-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bc98-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="1bc98-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1bc98-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


