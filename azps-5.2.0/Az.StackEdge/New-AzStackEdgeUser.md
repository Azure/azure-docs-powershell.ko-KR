---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324043"
---
# <span data-ttu-id="64322-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="64322-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="64322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64322-102">SYNOPSIS</span></span>
<span data-ttu-id="64322-103">디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64322-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="64322-104">구문</span><span class="sxs-lookup"><span data-stu-id="64322-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64322-105">설명</span><span class="sxs-lookup"><span data-stu-id="64322-105">DESCRIPTION</span></span>
<span data-ttu-id="64322-106">**New-AzStackEdgeUser** cmdlet은 Stack Edge 디바이스에 대한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64322-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="64322-107">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64322-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="64322-108">예제</span><span class="sxs-lookup"><span data-stu-id="64322-108">EXAMPLES</span></span>

### <span data-ttu-id="64322-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="64322-109">Example 1</span></span>
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

## <span data-ttu-id="64322-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64322-110">PARAMETERS</span></span>

### <span data-ttu-id="64322-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64322-111">-AsJob</span></span>
<span data-ttu-id="64322-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="64322-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64322-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64322-113">-DefaultProfile</span></span>
<span data-ttu-id="64322-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64322-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64322-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="64322-115">-DeviceName</span></span>
<span data-ttu-id="64322-116">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="64322-116">Device Name</span></span>

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

### <span data-ttu-id="64322-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="64322-117">-EncryptionKey</span></span>
<span data-ttu-id="64322-118">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="64322-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="64322-119">-Name</span><span class="sxs-lookup"><span data-stu-id="64322-119">-Name</span></span>
<span data-ttu-id="64322-120">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="64322-120">Username</span></span>

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

### <span data-ttu-id="64322-121">-Password</span><span class="sxs-lookup"><span data-stu-id="64322-121">-Password</span></span>
<span data-ttu-id="64322-122">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="64322-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="64322-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64322-123">-ResourceGroupName</span></span>
<span data-ttu-id="64322-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="64322-124">Resource Group Name</span></span>

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

### <span data-ttu-id="64322-125">-Type</span><span class="sxs-lookup"><span data-stu-id="64322-125">-Type</span></span>
<span data-ttu-id="64322-126">UserType 선택</span><span class="sxs-lookup"><span data-stu-id="64322-126">Select UserType</span></span>

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

### <span data-ttu-id="64322-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64322-127">-Confirm</span></span>
<span data-ttu-id="64322-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64322-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64322-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64322-129">-WhatIf</span></span>
<span data-ttu-id="64322-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="64322-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64322-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64322-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64322-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64322-132">CommonParameters</span></span>
<span data-ttu-id="64322-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64322-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64322-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64322-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64322-135">입력</span><span class="sxs-lookup"><span data-stu-id="64322-135">INPUTS</span></span>

### <span data-ttu-id="64322-136">없음</span><span class="sxs-lookup"><span data-stu-id="64322-136">None</span></span>

## <span data-ttu-id="64322-137">출력</span><span class="sxs-lookup"><span data-stu-id="64322-137">OUTPUTS</span></span>

### <span data-ttu-id="64322-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="64322-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="64322-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64322-139">NOTES</span></span>

## <span data-ttu-id="64322-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64322-140">RELATED LINKS</span></span>
