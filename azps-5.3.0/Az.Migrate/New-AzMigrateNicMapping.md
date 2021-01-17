---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385771"
---
# <span data-ttu-id="6f780-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="6f780-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="6f780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f780-102">SYNOPSIS</span></span>
<span data-ttu-id="6f780-103">복제 서버의 NIC 속성을 업데이트하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="6f780-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f780-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f780-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f780-105">DESCRIPTION</span></span>
<span data-ttu-id="6f780-106">New-AzMigrateNicMapping cmdlet은 마이그레이션할 서버에 연결된 원본 NIC의 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="6f780-107">이 개체는 복제 서버에 대한 NIC 및 해당 속성을 Set-AzMigrateServerReplication cmdlet에 대한 입력으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="6f780-108">예제</span><span class="sxs-lookup"><span data-stu-id="6f780-108">EXAMPLES</span></span>

### <span data-ttu-id="6f780-109">예제 1: NIC 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6f780-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="6f780-110">NIC 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="6f780-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f780-111">PARAMETERS</span></span>

### <span data-ttu-id="6f780-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="6f780-112">-NicID</span></span>
<span data-ttu-id="6f780-113">업데이트할 NIC의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f780-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="6f780-114">-TargetNicIP</span></span>
<span data-ttu-id="6f780-115">NIC에 사용할 대상 서브넷 내의 IP를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f780-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="6f780-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="6f780-117">업데이트할 NIC가 기본, 보조 또는 마이그레이션되지 않을지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f780-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="6f780-118">-TargetNicSubnet</span></span>
<span data-ttu-id="6f780-119">서버를 마이그레이션해야 하는 대상 Virtual Network의 NIC에 대한 서브넷 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f780-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f780-120">CommonParameters</span></span>
<span data-ttu-id="6f780-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f780-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f780-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f780-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f780-123">입력</span><span class="sxs-lookup"><span data-stu-id="6f780-123">INPUTS</span></span>

## <span data-ttu-id="6f780-124">출력</span><span class="sxs-lookup"><span data-stu-id="6f780-124">OUTPUTS</span></span>

### <span data-ttu-id="6f780-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="6f780-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="6f780-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f780-126">NOTES</span></span>

<span data-ttu-id="6f780-127">별칭</span><span class="sxs-lookup"><span data-stu-id="6f780-127">ALIASES</span></span>

## <span data-ttu-id="6f780-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f780-128">RELATED LINKS</span></span>

