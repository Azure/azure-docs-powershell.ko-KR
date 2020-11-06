---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: c75660c60788d5b2a099be97c927328464f34dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528698"
---
# <span data-ttu-id="005fe-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="005fe-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="005fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="005fe-102">SYNOPSIS</span></span>
<span data-ttu-id="005fe-103">구성 데이터베이스와 Git 리포지토리 간의 최근 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="005fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="005fe-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="005fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="005fe-105">DESCRIPTION</span></span>
<span data-ttu-id="005fe-106">**AzureRmApiManagementTenantSyncState** cmdlet은 구성 데이터베이스와 Git 리포지토리 간의 최신 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="005fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="005fe-107">EXAMPLES</span></span>

### <span data-ttu-id="005fe-108">예제 1: 최신 동기화 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="005fe-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="005fe-109">이 명령은 구성 데이터베이스와 Git 리포지토리 간에 가장 최근의 동기화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="005fe-110">변수</span><span class="sxs-lookup"><span data-stu-id="005fe-110">PARAMETERS</span></span>

### <span data-ttu-id="005fe-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="005fe-111">-Context</span></span>
<span data-ttu-id="005fe-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="005fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="005fe-113">-DefaultProfile</span></span>
<span data-ttu-id="005fe-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="005fe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005fe-115">CommonParameters</span></span>
<span data-ttu-id="005fe-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="005fe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005fe-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="005fe-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005fe-118">입력</span><span class="sxs-lookup"><span data-stu-id="005fe-118">INPUTS</span></span>

### <span data-ttu-id="005fe-119">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="005fe-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="005fe-120">출력</span><span class="sxs-lookup"><span data-stu-id="005fe-120">OUTPUTS</span></span>

### <span data-ttu-id="005fe-121">ApiManagement. ServiceManagement. \ PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="005fe-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="005fe-122">상속자</span><span class="sxs-lookup"><span data-stu-id="005fe-122">NOTES</span></span>

## <span data-ttu-id="005fe-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="005fe-123">RELATED LINKS</span></span>
