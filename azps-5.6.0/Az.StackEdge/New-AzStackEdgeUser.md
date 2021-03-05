---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: cd904a913ce9ea0cdcc2d347463fa21ac7e13943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005211"
---
# <span data-ttu-id="49c0f-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="49c0f-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="49c0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="49c0f-103">디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="49c0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="49c0f-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c0f-105">설명</span><span class="sxs-lookup"><span data-stu-id="49c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="49c0f-106">**New-AzStackEdgeUser** cmdlet은 Stack Edge 디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="49c0f-107">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="49c0f-108">예제</span><span class="sxs-lookup"><span data-stu-id="49c0f-108">EXAMPLES</span></span>

### <span data-ttu-id="49c0f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="49c0f-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="49c0f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49c0f-110">PARAMETERS</span></span>

### <span data-ttu-id="49c0f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49c0f-111">-AsJob</span></span>
<span data-ttu-id="49c0f-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="49c0f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49c0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c0f-113">-DefaultProfile</span></span>
<span data-ttu-id="49c0f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c0f-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="49c0f-115">-DeviceName</span></span>
<span data-ttu-id="49c0f-116">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="49c0f-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c0f-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="49c0f-117">-EncryptionKey</span></span>
<span data-ttu-id="49c0f-118">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="49c0f-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="49c0f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="49c0f-119">-Name</span></span>
<span data-ttu-id="49c0f-120">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="49c0f-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c0f-121">-Password</span><span class="sxs-lookup"><span data-stu-id="49c0f-121">-Password</span></span>
<span data-ttu-id="49c0f-122">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="49c0f-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="49c0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="49c0f-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="49c0f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c0f-125">-Type</span><span class="sxs-lookup"><span data-stu-id="49c0f-125">-Type</span></span>
<span data-ttu-id="49c0f-126">UserType 선택</span><span class="sxs-lookup"><span data-stu-id="49c0f-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c0f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="49c0f-127">-Confirm</span></span>
<span data-ttu-id="49c0f-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c0f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c0f-129">-WhatIf</span></span>
<span data-ttu-id="49c0f-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49c0f-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c0f-132">CommonParameters</span></span>
<span data-ttu-id="49c0f-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49c0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c0f-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c0f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c0f-135">입력</span><span class="sxs-lookup"><span data-stu-id="49c0f-135">INPUTS</span></span>

### <span data-ttu-id="49c0f-136">없음</span><span class="sxs-lookup"><span data-stu-id="49c0f-136">None</span></span>

## <span data-ttu-id="49c0f-137">출력</span><span class="sxs-lookup"><span data-stu-id="49c0f-137">OUTPUTS</span></span>

### <span data-ttu-id="49c0f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="49c0f-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="49c0f-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49c0f-139">NOTES</span></span>

## <span data-ttu-id="49c0f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49c0f-140">RELATED LINKS</span></span>
