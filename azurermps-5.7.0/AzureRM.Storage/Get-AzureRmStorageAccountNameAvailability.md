---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702137"
---
# <span data-ttu-id="8a10f-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8a10f-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="8a10f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a10f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a10f-103">저장소 계정 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a10f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a10f-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="8a10f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a10f-105">DESCRIPTION</span></span>
<span data-ttu-id="8a10f-106">**AzureRmStorageAccountNameAvailability** Cmdlet은 Azure 저장소 계정의 이름이 올바르며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="8a10f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a10f-107">EXAMPLES</span></span>

### <span data-ttu-id="8a10f-108">예제 1: 저장소 계정 이름의 사용 가능성 확인</span><span class="sxs-lookup"><span data-stu-id="8a10f-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="8a10f-109">이 명령은 이름 ContosoStorage03의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="8a10f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a10f-110">PARAMETERS</span></span>

### <span data-ttu-id="8a10f-111">-이름</span><span class="sxs-lookup"><span data-stu-id="8a10f-111">-Name</span></span>
<span data-ttu-id="8a10f-112">이 cmdlet이 확인 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="8a10f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a10f-113">CommonParameters</span></span>
<span data-ttu-id="8a10f-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a10f-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a10f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a10f-116">입력</span><span class="sxs-lookup"><span data-stu-id="8a10f-116">INPUTS</span></span>

### <span data-ttu-id="8a10f-117">않아야</span><span class="sxs-lookup"><span data-stu-id="8a10f-117">None</span></span>
<span data-ttu-id="8a10f-118">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a10f-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a10f-119">출력</span><span class="sxs-lookup"><span data-stu-id="8a10f-119">OUTPUTS</span></span>

## <span data-ttu-id="8a10f-120">상속자</span><span class="sxs-lookup"><span data-stu-id="8a10f-120">NOTES</span></span>

## <span data-ttu-id="8a10f-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a10f-121">RELATED LINKS</span></span>

[<span data-ttu-id="8a10f-122">Azure 저장소 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8a10f-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
