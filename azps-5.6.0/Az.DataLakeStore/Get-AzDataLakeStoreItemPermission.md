---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 0754160aa375ba84ac469771a97f792c36b51ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985194"
---
# <span data-ttu-id="b76ee-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b76ee-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="b76ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b76ee-103">Data Lake Store에서 파일 또는 폴더의 사용 권한 octal을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b76ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="b76ee-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76ee-105">설명</span><span class="sxs-lookup"><span data-stu-id="b76ee-105">DESCRIPTION</span></span>
<span data-ttu-id="b76ee-106">**Get-AzDataLakeStoreItemPermission** cmdlet은 Data Lake Store에서 파일 또는 폴더의 사용 권한 octal을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b76ee-107">예제</span><span class="sxs-lookup"><span data-stu-id="b76ee-107">EXAMPLES</span></span>

### <span data-ttu-id="b76ee-108">예제 1: 파일에 대한 사용 권한 octal 설정</span><span class="sxs-lookup"><span data-stu-id="b76ee-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="b76ee-109">이 명령은 파일에 대한 권한 octal을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="b76ee-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b76ee-110">PARAMETERS</span></span>

### <span data-ttu-id="b76ee-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b76ee-111">-Account</span></span>
<span data-ttu-id="b76ee-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="b76ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76ee-113">-DefaultProfile</span></span>
<span data-ttu-id="b76ee-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76ee-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b76ee-115">-Path</span></span>
<span data-ttu-id="b76ee-116">루트 디렉터리(/)로 시작하여 파일 또는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b76ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76ee-117">CommonParameters</span></span>
<span data-ttu-id="b76ee-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b76ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76ee-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b76ee-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76ee-120">입력</span><span class="sxs-lookup"><span data-stu-id="b76ee-120">INPUTS</span></span>

### <span data-ttu-id="b76ee-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b76ee-121">System.String</span></span>

### <span data-ttu-id="b76ee-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b76ee-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="b76ee-123">출력</span><span class="sxs-lookup"><span data-stu-id="b76ee-123">OUTPUTS</span></span>

### <span data-ttu-id="b76ee-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b76ee-124">System.String</span></span>

## <span data-ttu-id="b76ee-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b76ee-125">NOTES</span></span>
* <span data-ttu-id="b76ee-126">별칭: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b76ee-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="b76ee-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b76ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="b76ee-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b76ee-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


