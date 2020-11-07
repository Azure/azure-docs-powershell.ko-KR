---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696841"
---
# <span data-ttu-id="6f024-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="6f024-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="6f024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f024-102">SYNOPSIS</span></span>
<span data-ttu-id="6f024-103">Data Lake Store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6f024-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f024-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f024-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f024-105">DESCRIPTION</span></span>
<span data-ttu-id="6f024-106">**AzDataLakeStoreItemPermission** Cmdlet은 Data Lake store의 파일 또는 폴더에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6f024-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f024-107">EXAMPLES</span></span>

### <span data-ttu-id="6f024-108">예제 1: 파일에 대 한 사용 권한 8 진수 설정</span><span class="sxs-lookup"><span data-stu-id="6f024-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="6f024-109">이 명령은 파일에 대 한 사용 권한 8 진수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="6f024-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f024-110">PARAMETERS</span></span>

### <span data-ttu-id="6f024-111">-계정</span><span class="sxs-lookup"><span data-stu-id="6f024-111">-Account</span></span>
<span data-ttu-id="6f024-112">Data Lake Store 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6f024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f024-113">-DefaultProfile</span></span>
<span data-ttu-id="6f024-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f024-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6f024-115">-Path</span></span>
<span data-ttu-id="6f024-116">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6f024-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f024-117">CommonParameters</span></span>
<span data-ttu-id="6f024-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f024-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f024-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f024-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f024-120">입력</span><span class="sxs-lookup"><span data-stu-id="6f024-120">INPUTS</span></span>

### <span data-ttu-id="6f024-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f024-121">System.String</span></span>

### <span data-ttu-id="6f024-122">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="6f024-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="6f024-123">출력</span><span class="sxs-lookup"><span data-stu-id="6f024-123">OUTPUTS</span></span>

### <span data-ttu-id="6f024-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f024-124">System.String</span></span>

## <span data-ttu-id="6f024-125">상속자</span><span class="sxs-lookup"><span data-stu-id="6f024-125">NOTES</span></span>
* <span data-ttu-id="6f024-126">별칭: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="6f024-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="6f024-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f024-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f024-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="6f024-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)

