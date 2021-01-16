---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325072"
---
# <span data-ttu-id="8c63f-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8c63f-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="8c63f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c63f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c63f-103">Storage 계정 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="8c63f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c63f-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c63f-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c63f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c63f-106">**Get-AzStorageAccountNameAvailability** cmdlet은 Azure Storage 계정의 이름이 유효하고 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="8c63f-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c63f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c63f-108">예제 1: Storage 계정 이름의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="8c63f-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="8c63f-109">이 명령은 ContosoStorage03 이름의 가용성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="8c63f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c63f-110">PARAMETERS</span></span>

### <span data-ttu-id="8c63f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c63f-111">-DefaultProfile</span></span>
<span data-ttu-id="8c63f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c63f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8c63f-113">-Name</span></span>
<span data-ttu-id="8c63f-114">이 cmdlet이 검사하는 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="8c63f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c63f-115">CommonParameters</span></span>
<span data-ttu-id="8c63f-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c63f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c63f-117">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c63f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c63f-118">입력</span><span class="sxs-lookup"><span data-stu-id="8c63f-118">INPUTS</span></span>

### <span data-ttu-id="8c63f-119">System.String</span><span class="sxs-lookup"><span data-stu-id="8c63f-119">System.String</span></span>

## <span data-ttu-id="8c63f-120">출력</span><span class="sxs-lookup"><span data-stu-id="8c63f-120">OUTPUTS</span></span>

### <span data-ttu-id="8c63f-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="8c63f-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="8c63f-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c63f-122">NOTES</span></span>

## <span data-ttu-id="8c63f-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c63f-123">RELATED LINKS</span></span>

[<span data-ttu-id="8c63f-124">Azure Storage 관리자 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c63f-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


