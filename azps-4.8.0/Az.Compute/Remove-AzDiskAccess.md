---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056517"
---
# <span data-ttu-id="2b687-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2b687-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="2b687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b687-102">SYNOPSIS</span></span>
<span data-ttu-id="2b687-103">디스크 액세스 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="2b687-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b687-104">SYNTAX</span></span>

### <span data-ttu-id="2b687-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b687-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b687-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b687-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b687-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b687-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b687-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b687-108">DESCRIPTION</span></span>
<span data-ttu-id="2b687-109">**AzDiskAccess** cmdlet은 디스크 액세스 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="2b687-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b687-110">EXAMPLES</span></span>

### <span data-ttu-id="2b687-111">예제 1: 기본 매개 변수 집합을 사용 하 여 디스크 액세스 제거</span><span class="sxs-lookup"><span data-stu-id="2b687-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="2b687-112">이 명령은 리소스 그룹 "ResourceGroup01"에서 "DiskAccess01" 이라는 디스크 액세스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="2b687-113">예제 2: 리소스 ID를 사용 하 여 디스크 액세스 제거</span><span class="sxs-lookup"><span data-stu-id="2b687-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="2b687-114">이 명령은 리소스 ID를 기준으로 디스크 액세스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="2b687-115">예제 3: 입력 개체를 사용 하 여 디스크 액세스 제거</span><span class="sxs-lookup"><span data-stu-id="2b687-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="2b687-116">이 명령은 InputObject에서 디스크 액세스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="2b687-117">예제 4: 파이핑 입력 개체에의 한 디스크 액세스 제거</span><span class="sxs-lookup"><span data-stu-id="2b687-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="2b687-118">이 명령은 InputObject를 파이핑 하 여 디스크 액세스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="2b687-119">변수</span><span class="sxs-lookup"><span data-stu-id="2b687-119">PARAMETERS</span></span>

### <span data-ttu-id="2b687-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b687-120">-AsJob</span></span>
<span data-ttu-id="2b687-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2b687-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b687-122">-DefaultProfile</span></span>
<span data-ttu-id="2b687-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b687-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b687-124">-InputObject</span></span>
<span data-ttu-id="2b687-125">PowerShell 디스크 액세스 개체</span><span class="sxs-lookup"><span data-stu-id="2b687-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-126">-이름</span><span class="sxs-lookup"><span data-stu-id="2b687-126">-Name</span></span>
<span data-ttu-id="2b687-127">디스크 액세스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b687-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b687-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b687-130">-ResourceId</span></span>
<span data-ttu-id="2b687-131">디스크 액세스에 대 한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-132">-확인</span><span class="sxs-lookup"><span data-stu-id="2b687-132">-Confirm</span></span>
<span data-ttu-id="2b687-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b687-134">-WhatIf</span></span>
<span data-ttu-id="2b687-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b687-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b687-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b687-137">CommonParameters</span></span>
<span data-ttu-id="2b687-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b687-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b687-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b687-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b687-140">입력</span><span class="sxs-lookup"><span data-stu-id="2b687-140">INPUTS</span></span>

### <span data-ttu-id="2b687-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b687-141">System.String</span></span>

### <span data-ttu-id="2b687-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2b687-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="2b687-143">출력</span><span class="sxs-lookup"><span data-stu-id="2b687-143">OUTPUTS</span></span>

### <span data-ttu-id="2b687-144">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="2b687-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2b687-145">상속자</span><span class="sxs-lookup"><span data-stu-id="2b687-145">NOTES</span></span>

## <span data-ttu-id="2b687-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b687-146">RELATED LINKS</span></span>
