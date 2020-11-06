---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526520"
---
# <span data-ttu-id="56852-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="56852-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="56852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56852-102">SYNOPSIS</span></span>
<span data-ttu-id="56852-103">Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56852-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56852-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56852-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="56852-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56852-105">DESCRIPTION</span></span>
<span data-ttu-id="56852-106">**AzureRmStorageAccountKey** Cmdlet은 Azure 저장소 계정의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56852-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="56852-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56852-107">EXAMPLES</span></span>

### <span data-ttu-id="56852-108">예제 1: 저장소 계정의 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="56852-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="56852-109">이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56852-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="56852-110">예제 2: 저장소 계정에 대 한 특정 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="56852-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="56852-111">변수</span><span class="sxs-lookup"><span data-stu-id="56852-111">PARAMETERS</span></span>

### <span data-ttu-id="56852-112">-이름</span><span class="sxs-lookup"><span data-stu-id="56852-112">-Name</span></span>
<span data-ttu-id="56852-113">이 cmdlet에서 키를 가져오는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56852-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56852-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56852-114">-ResourceGroupName</span></span>
<span data-ttu-id="56852-115">저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56852-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56852-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56852-116">CommonParameters</span></span>
<span data-ttu-id="56852-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56852-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56852-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56852-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56852-119">입력</span><span class="sxs-lookup"><span data-stu-id="56852-119">INPUTS</span></span>

### <span data-ttu-id="56852-120">않아야</span><span class="sxs-lookup"><span data-stu-id="56852-120">None</span></span>
<span data-ttu-id="56852-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56852-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56852-122">출력</span><span class="sxs-lookup"><span data-stu-id="56852-122">OUTPUTS</span></span>

## <span data-ttu-id="56852-123">상속자</span><span class="sxs-lookup"><span data-stu-id="56852-123">NOTES</span></span>

## <span data-ttu-id="56852-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56852-124">RELATED LINKS</span></span>

[<span data-ttu-id="56852-125">새로운 AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="56852-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
