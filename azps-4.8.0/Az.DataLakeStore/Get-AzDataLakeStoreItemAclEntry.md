---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214575"
---
# <span data-ttu-id="cea9e-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cea9e-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="cea9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="cea9e-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cea9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cea9e-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cea9e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cea9e-105">DESCRIPTION</span></span>
<span data-ttu-id="cea9e-106">**AzDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)에 있는 항목 (ACE)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cea9e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cea9e-107">EXAMPLES</span></span>

### <span data-ttu-id="cea9e-108">예제 1: 폴더에 대 한 ACL 가져오기</span><span class="sxs-lookup"><span data-stu-id="cea9e-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="cea9e-109">이 명령은 지정 된 Data Lake Store 계정의 루트 디렉터리에 대 한 ACL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="cea9e-110">변수</span><span class="sxs-lookup"><span data-stu-id="cea9e-110">PARAMETERS</span></span>

### <span data-ttu-id="cea9e-111">-계정</span><span class="sxs-lookup"><span data-stu-id="cea9e-111">-Account</span></span>
<span data-ttu-id="cea9e-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cea9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea9e-113">-DefaultProfile</span></span>
<span data-ttu-id="cea9e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea9e-115">-Path</span><span class="sxs-lookup"><span data-stu-id="cea9e-115">-Path</span></span>
<span data-ttu-id="cea9e-116">이 cmdlet에서 ACE를 가져오는 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cea9e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea9e-117">CommonParameters</span></span>
<span data-ttu-id="cea9e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cea9e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea9e-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea9e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea9e-120">입력</span><span class="sxs-lookup"><span data-stu-id="cea9e-120">INPUTS</span></span>

### <span data-ttu-id="cea9e-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cea9e-121">System.String</span></span>

### <span data-ttu-id="cea9e-122">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="cea9e-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="cea9e-123">출력</span><span class="sxs-lookup"><span data-stu-id="cea9e-123">OUTPUTS</span></span>

### <span data-ttu-id="cea9e-124">DataLakeStore. DataLakeStoreItemAce/.</span><span class="sxs-lookup"><span data-stu-id="cea9e-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="cea9e-125">상속자</span><span class="sxs-lookup"><span data-stu-id="cea9e-125">NOTES</span></span>

## <span data-ttu-id="cea9e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cea9e-126">RELATED LINKS</span></span>

[<span data-ttu-id="cea9e-127">제거-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cea9e-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="cea9e-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cea9e-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


