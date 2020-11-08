---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211647"
---
# <span data-ttu-id="58ce3-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="58ce3-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="58ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="58ce3-103">공개 유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ce3-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="58ce3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58ce3-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ce3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="58ce3-106">공개 유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ce3-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="58ce3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="58ce3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="58ce3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="58ce3-109">공개 유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ce3-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="58ce3-110">변수</span><span class="sxs-lookup"><span data-stu-id="58ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="58ce3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ce3-111">-DefaultProfile</span></span>
<span data-ttu-id="58ce3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58ce3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ce3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="58ce3-113">-Name</span></span>
<span data-ttu-id="58ce3-114">공개 유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58ce3-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ce3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ce3-115">-ResourceGroupName</span></span>
<span data-ttu-id="58ce3-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58ce3-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ce3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ce3-117">CommonParameters</span></span>
<span data-ttu-id="58ce3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ce3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ce3-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58ce3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ce3-120">입력</span><span class="sxs-lookup"><span data-stu-id="58ce3-120">INPUTS</span></span>

### <span data-ttu-id="58ce3-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58ce3-121">System.String</span></span>

## <span data-ttu-id="58ce3-122">출력</span><span class="sxs-lookup"><span data-stu-id="58ce3-122">OUTPUTS</span></span>

### <span data-ttu-id="58ce3-123">PSMaintenanceConfiguration/. m m</span><span class="sxs-lookup"><span data-stu-id="58ce3-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="58ce3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="58ce3-124">NOTES</span></span>

## <span data-ttu-id="58ce3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58ce3-125">RELATED LINKS</span></span>
