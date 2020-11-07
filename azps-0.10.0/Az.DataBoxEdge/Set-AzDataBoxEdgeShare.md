---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac4f7814898bcbfcee75c4a31273dfbcb6be7335
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875964"
---
# <span data-ttu-id="b1370-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b1370-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="b1370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1370-102">SYNOPSIS</span></span>
<span data-ttu-id="b1370-103">장치에 대 한 공유를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-103">Updates the share for a device.</span></span>

## <span data-ttu-id="b1370-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1370-104">SYNTAX</span></span>

### <span data-ttu-id="b1370-105">SmbParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1370-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1370-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1370-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1370-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1370-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1370-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1370-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1370-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1370-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1370-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1370-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1370-111">설명은</span><span class="sxs-lookup"><span data-stu-id="b1370-111">DESCRIPTION</span></span>
<span data-ttu-id="b1370-112">이 **Set-AzDataBoxEdgeShare** 는 액세스 권한을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="b1370-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b1370-113">EXAMPLES</span></span>

### <span data-ttu-id="b1370-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1370-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="b1370-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b1370-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="b1370-116">변수</span><span class="sxs-lookup"><span data-stu-id="b1370-116">PARAMETERS</span></span>

### <span data-ttu-id="b1370-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1370-117">-AsJob</span></span>
<span data-ttu-id="b1370-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b1370-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1370-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="b1370-119">-ClientAccessRight</span></span>
<span data-ttu-id="b1370-120">Ds (예: @ {"ClientId" = "192.168.10.10)에 대 한 읽기/쓰기 액세스 AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="b1370-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1370-121">-DefaultProfile</span></span>
<span data-ttu-id="b1370-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1370-123">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="b1370-123">-DeviceName</span></span>
<span data-ttu-id="b1370-124">장치 이름</span><span class="sxs-lookup"><span data-stu-id="b1370-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1370-125">-InputObject</span></span>
<span data-ttu-id="b1370-126">입력 개체</span><span class="sxs-lookup"><span data-stu-id="b1370-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-127">-이름</span><span class="sxs-lookup"><span data-stu-id="b1370-127">-Name</span></span>
<span data-ttu-id="b1370-128">자원 이름</span><span class="sxs-lookup"><span data-stu-id="b1370-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1370-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1370-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b1370-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1370-131">-ResourceId</span></span>
<span data-ttu-id="b1370-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1370-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="b1370-133">-UserAccessRight</span></span>
<span data-ttu-id="b1370-134">예: @ (@ {"Username" = "user-name-1")에 액세스할 수 있도록 기존 사용자 이름과 함께 액세스 권한을 제공 합니다. AccessRight "=" Read "}, @ {" Username "=" 사용자 이름-2 ";" AccessRight "=" Read "}, @ {" Username "=" 사용자 이름-3 ";" AccessRight "=" 사용자 지정 "})</span><span class="sxs-lookup"><span data-stu-id="b1370-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1370-135">-확인</span><span class="sxs-lookup"><span data-stu-id="b1370-135">-Confirm</span></span>
<span data-ttu-id="b1370-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1370-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1370-137">-WhatIf</span></span>
<span data-ttu-id="b1370-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1370-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1370-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1370-140">CommonParameters</span></span>
<span data-ttu-id="b1370-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1370-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1370-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1370-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1370-143">입력</span><span class="sxs-lookup"><span data-stu-id="b1370-143">INPUTS</span></span>

### <span data-ttu-id="b1370-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1370-144">System.String</span></span>

### <span data-ttu-id="b1370-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b1370-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="b1370-146">출력</span><span class="sxs-lookup"><span data-stu-id="b1370-146">OUTPUTS</span></span>

### <span data-ttu-id="b1370-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b1370-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="b1370-148">상속자</span><span class="sxs-lookup"><span data-stu-id="b1370-148">NOTES</span></span>

## <span data-ttu-id="b1370-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1370-149">RELATED LINKS</span></span>
