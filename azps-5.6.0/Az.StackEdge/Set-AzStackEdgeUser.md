---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 0c3494e96290702c424a8e8bac7680daa376c488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994868"
---
# <span data-ttu-id="d8dd5-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="d8dd5-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="d8dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dd5-103">디바이스의 사용자에 대한 새 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="d8dd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8dd5-104">SYNTAX</span></span>

### <span data-ttu-id="d8dd5-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8dd5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8dd5-108">설명</span><span class="sxs-lookup"><span data-stu-id="d8dd5-108">DESCRIPTION</span></span>
<span data-ttu-id="d8dd5-109">**Set-AzStackEdgeUser** cmdlet은 Stack Edge 디바이스의 사용자에 대한 새 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="d8dd5-110">예제</span><span class="sxs-lookup"><span data-stu-id="d8dd5-110">EXAMPLES</span></span>

### <span data-ttu-id="d8dd5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8dd5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="d8dd5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8dd5-112">PARAMETERS</span></span>

### <span data-ttu-id="d8dd5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8dd5-113">-AsJob</span></span>
<span data-ttu-id="d8dd5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8dd5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8dd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dd5-115">-DefaultProfile</span></span>
<span data-ttu-id="d8dd5-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dd5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d8dd5-117">-DeviceName</span></span>
<span data-ttu-id="d8dd5-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="d8dd5-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd5-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d8dd5-119">-EncryptionKey</span></span>
<span data-ttu-id="d8dd5-120">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="d8dd5-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d8dd5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8dd5-121">-InputObject</span></span>
<span data-ttu-id="d8dd5-122">입력 개체</span><span class="sxs-lookup"><span data-stu-id="d8dd5-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d8dd5-123">-Name</span></span>
<span data-ttu-id="d8dd5-124">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="d8dd5-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd5-125">-Password</span><span class="sxs-lookup"><span data-stu-id="d8dd5-125">-Password</span></span>
<span data-ttu-id="d8dd5-126">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="d8dd5-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="d8dd5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dd5-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8dd5-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d8dd5-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dd5-129">-ResourceId</span></span>
<span data-ttu-id="d8dd5-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dd5-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd5-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d8dd5-131">-Confirm</span></span>
<span data-ttu-id="d8dd5-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dd5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8dd5-133">-WhatIf</span></span>
<span data-ttu-id="d8dd5-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8dd5-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dd5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dd5-136">CommonParameters</span></span>
<span data-ttu-id="d8dd5-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8dd5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dd5-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8dd5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dd5-139">입력</span><span class="sxs-lookup"><span data-stu-id="d8dd5-139">INPUTS</span></span>

### <span data-ttu-id="d8dd5-140">없음</span><span class="sxs-lookup"><span data-stu-id="d8dd5-140">None</span></span>

## <span data-ttu-id="d8dd5-141">출력</span><span class="sxs-lookup"><span data-stu-id="d8dd5-141">OUTPUTS</span></span>

### <span data-ttu-id="d8dd5-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="d8dd5-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="d8dd5-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8dd5-143">NOTES</span></span>

## <span data-ttu-id="d8dd5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8dd5-144">RELATED LINKS</span></span>
