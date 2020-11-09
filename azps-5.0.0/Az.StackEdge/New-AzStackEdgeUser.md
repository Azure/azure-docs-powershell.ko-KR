---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310574"
---
# <span data-ttu-id="220fb-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="220fb-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="220fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="220fb-102">SYNOPSIS</span></span>
<span data-ttu-id="220fb-103">장치에 대 한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="220fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="220fb-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="220fb-105">DESCRIPTION</span></span>
<span data-ttu-id="220fb-106">**AzStackEdgeUser** Cmdlet은 스택 가장자리 장치에 대 한 새 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="220fb-107">유형의 사용자 만들기만 `Share` 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="220fb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="220fb-108">EXAMPLES</span></span>

### <span data-ttu-id="220fb-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="220fb-109">Example 1</span></span>
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

## <span data-ttu-id="220fb-110">변수</span><span class="sxs-lookup"><span data-stu-id="220fb-110">PARAMETERS</span></span>

### <span data-ttu-id="220fb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="220fb-111">-AsJob</span></span>
<span data-ttu-id="220fb-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="220fb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="220fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220fb-113">-DefaultProfile</span></span>
<span data-ttu-id="220fb-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220fb-115">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="220fb-115">-DeviceName</span></span>
<span data-ttu-id="220fb-116">장치 이름</span><span class="sxs-lookup"><span data-stu-id="220fb-116">Device Name</span></span>

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

### <span data-ttu-id="220fb-117">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="220fb-117">-EncryptionKey</span></span>
<span data-ttu-id="220fb-118">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="220fb-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="220fb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="220fb-119">-Name</span></span>
<span data-ttu-id="220fb-120">사용자</span><span class="sxs-lookup"><span data-stu-id="220fb-120">Username</span></span>

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

### <span data-ttu-id="220fb-121">-암호</span><span class="sxs-lookup"><span data-stu-id="220fb-121">-Password</span></span>
<span data-ttu-id="220fb-122">암호, 보안 문자열로 제공</span><span class="sxs-lookup"><span data-stu-id="220fb-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="220fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="220fb-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="220fb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="220fb-125">-Type</span><span class="sxs-lookup"><span data-stu-id="220fb-125">-Type</span></span>
<span data-ttu-id="220fb-126">UserType 선택</span><span class="sxs-lookup"><span data-stu-id="220fb-126">Select UserType</span></span>

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

### <span data-ttu-id="220fb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="220fb-127">-Confirm</span></span>
<span data-ttu-id="220fb-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220fb-129">-WhatIf</span></span>
<span data-ttu-id="220fb-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="220fb-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220fb-132">CommonParameters</span></span>
<span data-ttu-id="220fb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="220fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220fb-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="220fb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220fb-135">입력</span><span class="sxs-lookup"><span data-stu-id="220fb-135">INPUTS</span></span>

### <span data-ttu-id="220fb-136">않아야</span><span class="sxs-lookup"><span data-stu-id="220fb-136">None</span></span>

## <span data-ttu-id="220fb-137">출력</span><span class="sxs-lookup"><span data-stu-id="220fb-137">OUTPUTS</span></span>

### <span data-ttu-id="220fb-138">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="220fb-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="220fb-139">상속자</span><span class="sxs-lookup"><span data-stu-id="220fb-139">NOTES</span></span>

## <span data-ttu-id="220fb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="220fb-140">RELATED LINKS</span></span>
