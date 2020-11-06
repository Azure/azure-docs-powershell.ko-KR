---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534128"
---
# <span data-ttu-id="20d4e-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="20d4e-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="20d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="20d4e-103">Data Lake Store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20d4e-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20d4e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="20d4e-106">**AzureRmDataLakeStoreItemPermission** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="20d4e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20d4e-107">EXAMPLES</span></span>

### <span data-ttu-id="20d4e-108">예제 1: 파일에 대 한 사용 권한 8 진수 설정</span><span class="sxs-lookup"><span data-stu-id="20d4e-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="20d4e-109">이 명령은 파일에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="20d4e-110">변수</span><span class="sxs-lookup"><span data-stu-id="20d4e-110">PARAMETERS</span></span>

### <span data-ttu-id="20d4e-111">-계정</span><span class="sxs-lookup"><span data-stu-id="20d4e-111">-Account</span></span>
<span data-ttu-id="20d4e-112">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="20d4e-113">-Path</span><span class="sxs-lookup"><span data-stu-id="20d4e-113">-Path</span></span>
<span data-ttu-id="20d4e-114">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="20d4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d4e-115">-DefaultProfile</span></span>
<span data-ttu-id="20d4e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d4e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d4e-117">CommonParameters</span></span>
<span data-ttu-id="20d4e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20d4e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d4e-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d4e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d4e-120">입력</span><span class="sxs-lookup"><span data-stu-id="20d4e-120">INPUTS</span></span>

## <span data-ttu-id="20d4e-121">출력</span><span class="sxs-lookup"><span data-stu-id="20d4e-121">OUTPUTS</span></span>

### <span data-ttu-id="20d4e-122">이름</span><span class="sxs-lookup"><span data-stu-id="20d4e-122">string</span></span>
<span data-ttu-id="20d4e-123">소유 지분 8 진수의 문자열 표현</span><span class="sxs-lookup"><span data-stu-id="20d4e-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="20d4e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="20d4e-124">NOTES</span></span>
* <span data-ttu-id="20d4e-125">별칭: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="20d4e-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="20d4e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20d4e-126">RELATED LINKS</span></span>

[<span data-ttu-id="20d4e-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="20d4e-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


