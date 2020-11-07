---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: c344d5ac901e45c92c04a23cee252b1f747d4a83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875962"
---
# <span data-ttu-id="7d5a5-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7d5a5-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="7d5a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5a5-103">디바이스의 사용자에 대 한 새 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="7d5a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d5a5-104">SYNTAX</span></span>

### <span data-ttu-id="7d5a5-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d5a5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d5a5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d5a5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d5a5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d5a5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d5a5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7d5a5-108">DESCRIPTION</span></span>
<span data-ttu-id="7d5a5-109">**AzDataBoxEdgeUser** Cmdlet은 데이터 상자 가장자리 장치에서 사용자에 대 한 새 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="7d5a5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7d5a5-110">EXAMPLES</span></span>

### <span data-ttu-id="7d5a5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d5a5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="7d5a5-112">변수</span><span class="sxs-lookup"><span data-stu-id="7d5a5-112">PARAMETERS</span></span>

### <span data-ttu-id="7d5a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d5a5-113">-AsJob</span></span>
<span data-ttu-id="7d5a5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7d5a5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d5a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5a5-115">-DefaultProfile</span></span>
<span data-ttu-id="7d5a5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d5a5-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="7d5a5-117">-DeviceName</span></span>
<span data-ttu-id="7d5a5-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="7d5a5-118">Device Name</span></span>

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

### <span data-ttu-id="7d5a5-119">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="7d5a5-119">-EncryptionKey</span></span>
<span data-ttu-id="7d5a5-120">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="7d5a5-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="7d5a5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d5a5-121">-InputObject</span></span>
<span data-ttu-id="7d5a5-122">입력 개체</span><span class="sxs-lookup"><span data-stu-id="7d5a5-122">Input Object</span></span>

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

### <span data-ttu-id="7d5a5-123">-이름</span><span class="sxs-lookup"><span data-stu-id="7d5a5-123">-Name</span></span>
<span data-ttu-id="7d5a5-124">사용자</span><span class="sxs-lookup"><span data-stu-id="7d5a5-124">Username</span></span>

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

### <span data-ttu-id="7d5a5-125">-암호</span><span class="sxs-lookup"><span data-stu-id="7d5a5-125">-Password</span></span>
<span data-ttu-id="7d5a5-126">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="7d5a5-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="7d5a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d5a5-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7d5a5-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7d5a5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d5a5-129">-ResourceId</span></span>
<span data-ttu-id="7d5a5-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d5a5-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="7d5a5-131">-확인</span><span class="sxs-lookup"><span data-stu-id="7d5a5-131">-Confirm</span></span>
<span data-ttu-id="7d5a5-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d5a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d5a5-133">-WhatIf</span></span>
<span data-ttu-id="7d5a5-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d5a5-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d5a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5a5-136">CommonParameters</span></span>
<span data-ttu-id="7d5a5-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5a5-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5a5-139">입력</span><span class="sxs-lookup"><span data-stu-id="7d5a5-139">INPUTS</span></span>

### <span data-ttu-id="7d5a5-140">않아야</span><span class="sxs-lookup"><span data-stu-id="7d5a5-140">None</span></span>

## <span data-ttu-id="7d5a5-141">출력</span><span class="sxs-lookup"><span data-stu-id="7d5a5-141">OUTPUTS</span></span>

### <span data-ttu-id="7d5a5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7d5a5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="7d5a5-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7d5a5-143">NOTES</span></span>

## <span data-ttu-id="7d5a5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d5a5-144">RELATED LINKS</span></span>
