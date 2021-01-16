---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343857"
---
# <span data-ttu-id="4eba9-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4eba9-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="4eba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eba9-102">SYNOPSIS</span></span>
<span data-ttu-id="4eba9-103">Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4eba9-104">구문</span><span class="sxs-lookup"><span data-stu-id="4eba9-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eba9-105">설명</span><span class="sxs-lookup"><span data-stu-id="4eba9-105">DESCRIPTION</span></span>
<span data-ttu-id="4eba9-106">**Get-AzDataLakeStoreItemPermission** cmdlet은 Data Lake Store에서 파일 또는 폴더의 사용 권한 8진수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4eba9-107">예제</span><span class="sxs-lookup"><span data-stu-id="4eba9-107">EXAMPLES</span></span>

### <span data-ttu-id="4eba9-108">예제 1: 파일에 대한 사용 권한 8진수 설정</span><span class="sxs-lookup"><span data-stu-id="4eba9-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="4eba9-109">이 명령은 파일에 대한 권한 8진수 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="4eba9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eba9-110">PARAMETERS</span></span>

### <span data-ttu-id="4eba9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4eba9-111">-Account</span></span>
<span data-ttu-id="4eba9-112">Data Lake Store 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="4eba9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eba9-113">-DefaultProfile</span></span>
<span data-ttu-id="4eba9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eba9-115">-Path</span><span class="sxs-lookup"><span data-stu-id="4eba9-115">-Path</span></span>
<span data-ttu-id="4eba9-116">루트 디렉터리(/)로 시작하는 파일 또는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4eba9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eba9-117">CommonParameters</span></span>
<span data-ttu-id="4eba9-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4eba9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eba9-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4eba9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eba9-120">입력</span><span class="sxs-lookup"><span data-stu-id="4eba9-120">INPUTS</span></span>

### <span data-ttu-id="4eba9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4eba9-121">System.String</span></span>

### <span data-ttu-id="4eba9-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4eba9-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="4eba9-123">출력</span><span class="sxs-lookup"><span data-stu-id="4eba9-123">OUTPUTS</span></span>

### <span data-ttu-id="4eba9-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4eba9-124">System.String</span></span>

## <span data-ttu-id="4eba9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4eba9-125">NOTES</span></span>
* <span data-ttu-id="4eba9-126">별칭: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4eba9-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="4eba9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eba9-127">RELATED LINKS</span></span>

[<span data-ttu-id="4eba9-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="4eba9-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


