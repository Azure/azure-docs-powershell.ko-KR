---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
ms.openlocfilehash: 5371b5c54cfaff4b1c48dd8a8643e0cc51b1e00e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881229"
---
# <span data-ttu-id="549ec-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="549ec-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="549ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549ec-102">SYNOPSIS</span></span>
<span data-ttu-id="549ec-103">저장소 계정 이름의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="549ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="549ec-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="549ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="549ec-105">DESCRIPTION</span></span>
<span data-ttu-id="549ec-106">**AzureRmStorageAccountNameAvailability** Cmdlet은 Azure 저장소 계정의 이름이 올바르며 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="549ec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="549ec-107">EXAMPLES</span></span>

### <span data-ttu-id="549ec-108">예제 1: 저장소 계정 이름의 사용 가능성 확인</span><span class="sxs-lookup"><span data-stu-id="549ec-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="549ec-109">이 명령은 이름 ContosoStorage03의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="549ec-110">변수</span><span class="sxs-lookup"><span data-stu-id="549ec-110">PARAMETERS</span></span>

### <span data-ttu-id="549ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549ec-111">-DefaultProfile</span></span>
<span data-ttu-id="549ec-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549ec-113">-이름</span><span class="sxs-lookup"><span data-stu-id="549ec-113">-Name</span></span>
<span data-ttu-id="549ec-114">이 cmdlet이 확인 하는 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="549ec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549ec-115">CommonParameters</span></span>
<span data-ttu-id="549ec-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549ec-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549ec-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549ec-118">입력</span><span class="sxs-lookup"><span data-stu-id="549ec-118">INPUTS</span></span>

### <span data-ttu-id="549ec-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="549ec-119">System.String</span></span>

## <span data-ttu-id="549ec-120">출력</span><span class="sxs-lookup"><span data-stu-id="549ec-120">OUTPUTS</span></span>

### <span data-ttu-id="549ec-121">CheckNameAvailabilityResult를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="549ec-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="549ec-122">상속자</span><span class="sxs-lookup"><span data-stu-id="549ec-122">NOTES</span></span>

## <span data-ttu-id="549ec-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="549ec-123">RELATED LINKS</span></span>

[<span data-ttu-id="549ec-124">Azure 저장소 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="549ec-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


