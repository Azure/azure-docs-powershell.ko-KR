---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494418"
---
# <span data-ttu-id="14210-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="14210-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="14210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14210-102">SYNOPSIS</span></span>
<span data-ttu-id="14210-103">구성 데이터베이스와 Git 리포지토리 간의 가장 최근 동기화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14210-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="14210-104">구문</span><span class="sxs-lookup"><span data-stu-id="14210-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14210-105">설명</span><span class="sxs-lookup"><span data-stu-id="14210-105">DESCRIPTION</span></span>
<span data-ttu-id="14210-106">**Get-AzApiManagementTenantSyncState** cmdlet은 구성 데이터베이스와 Git 리포지토리 간의 가장 최근 동기화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14210-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="14210-107">예제</span><span class="sxs-lookup"><span data-stu-id="14210-107">EXAMPLES</span></span>

### <span data-ttu-id="14210-108">예제 1: 가장 최근 동기화의 상태 확인</span><span class="sxs-lookup"><span data-stu-id="14210-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="14210-109">이 명령은 구성 데이터베이스와 Git 리포지토리 간의 가장 최근 동기화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14210-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="14210-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14210-110">PARAMETERS</span></span>

### <span data-ttu-id="14210-111">-Context</span><span class="sxs-lookup"><span data-stu-id="14210-111">-Context</span></span>
<span data-ttu-id="14210-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="14210-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14210-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14210-113">-DefaultProfile</span></span>
<span data-ttu-id="14210-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14210-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14210-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14210-115">CommonParameters</span></span>
<span data-ttu-id="14210-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14210-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14210-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14210-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14210-118">입력</span><span class="sxs-lookup"><span data-stu-id="14210-118">INPUTS</span></span>

### <span data-ttu-id="14210-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14210-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="14210-120">출력</span><span class="sxs-lookup"><span data-stu-id="14210-120">OUTPUTS</span></span>

### <span data-ttu-id="14210-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="14210-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="14210-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14210-122">NOTES</span></span>

## <span data-ttu-id="14210-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14210-123">RELATED LINKS</span></span>
