---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345981"
---
# <span data-ttu-id="4eb57-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4eb57-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="4eb57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb57-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb57-103">디바이스에서 사용자에 대한 새 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="4eb57-104">구문</span><span class="sxs-lookup"><span data-stu-id="4eb57-104">SYNTAX</span></span>

### <span data-ttu-id="4eb57-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4eb57-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb57-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb57-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb57-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb57-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb57-108">설명</span><span class="sxs-lookup"><span data-stu-id="4eb57-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb57-109">**Set-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에서 사용자에 대한 새 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="4eb57-110">예제</span><span class="sxs-lookup"><span data-stu-id="4eb57-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb57-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4eb57-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="4eb57-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb57-112">PARAMETERS</span></span>

### <span data-ttu-id="4eb57-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eb57-113">-AsJob</span></span>
<span data-ttu-id="4eb57-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4eb57-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4eb57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb57-115">-DefaultProfile</span></span>
<span data-ttu-id="4eb57-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb57-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4eb57-117">-DeviceName</span></span>
<span data-ttu-id="4eb57-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="4eb57-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4eb57-119">-EncryptionKey</span></span>
<span data-ttu-id="4eb57-120">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="4eb57-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb57-121">-InputObject</span></span>
<span data-ttu-id="4eb57-122">입력 개체</span><span class="sxs-lookup"><span data-stu-id="4eb57-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb57-123">-Name</span></span>
<span data-ttu-id="4eb57-124">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="4eb57-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-125">-Password</span><span class="sxs-lookup"><span data-stu-id="4eb57-125">-Password</span></span>
<span data-ttu-id="4eb57-126">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="4eb57-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb57-127">-ResourceGroupName</span></span>
<span data-ttu-id="4eb57-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4eb57-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb57-129">-ResourceId</span></span>
<span data-ttu-id="4eb57-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb57-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb57-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb57-131">-Confirm</span></span>
<span data-ttu-id="4eb57-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb57-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb57-133">-WhatIf</span></span>
<span data-ttu-id="4eb57-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4eb57-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4eb57-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb57-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb57-136">CommonParameters</span></span>
<span data-ttu-id="4eb57-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb57-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb57-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4eb57-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb57-139">입력</span><span class="sxs-lookup"><span data-stu-id="4eb57-139">INPUTS</span></span>

### <span data-ttu-id="4eb57-140">없음</span><span class="sxs-lookup"><span data-stu-id="4eb57-140">None</span></span>

## <span data-ttu-id="4eb57-141">출력</span><span class="sxs-lookup"><span data-stu-id="4eb57-141">OUTPUTS</span></span>

### <span data-ttu-id="4eb57-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4eb57-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="4eb57-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4eb57-143">NOTES</span></span>

## <span data-ttu-id="4eb57-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eb57-144">RELATED LINKS</span></span>
