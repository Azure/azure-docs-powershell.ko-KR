---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194665"
---
# <span data-ttu-id="b35ba-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b35ba-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="b35ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b35ba-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b35ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="b35ba-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b35ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="b35ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b35ba-106">**Get-AzDataLakeStoreItemAclEntry** cmdlet은 Data Lake Store의 파일 또는 폴더의 ACL(액세스 제어 목록)에서 ACE(항목)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b35ba-107">예제</span><span class="sxs-lookup"><span data-stu-id="b35ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b35ba-108">예제 1: 폴더에 대한 ACL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="b35ba-109">이 명령은 지정된 Data Lake Store 계정의 루트 디렉터리에 대한 ACL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="b35ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b35ba-110">PARAMETERS</span></span>

### <span data-ttu-id="b35ba-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b35ba-111">-Account</span></span>
<span data-ttu-id="b35ba-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b35ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35ba-113">-DefaultProfile</span></span>
<span data-ttu-id="b35ba-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b35ba-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b35ba-115">-Path</span></span>
<span data-ttu-id="b35ba-116">이 cmdlet이 루트 디렉터리(/)로 시작하는 ACE를 얻을 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b35ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35ba-117">CommonParameters</span></span>
<span data-ttu-id="b35ba-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b35ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35ba-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b35ba-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35ba-120">입력</span><span class="sxs-lookup"><span data-stu-id="b35ba-120">INPUTS</span></span>

### <span data-ttu-id="b35ba-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b35ba-121">System.String</span></span>

### <span data-ttu-id="b35ba-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b35ba-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="b35ba-123">출력</span><span class="sxs-lookup"><span data-stu-id="b35ba-123">OUTPUTS</span></span>

### <span data-ttu-id="b35ba-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="b35ba-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="b35ba-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b35ba-125">NOTES</span></span>

## <span data-ttu-id="b35ba-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b35ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="b35ba-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b35ba-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="b35ba-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b35ba-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


