---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968640"
---
# <span data-ttu-id="df8ae-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="df8ae-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="df8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="df8ae-103">ANF(Azure NetApp Files) Active Directory 구성에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="df8ae-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="df8ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="df8ae-104">SYNTAX</span></span>

### <span data-ttu-id="df8ae-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="df8ae-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df8ae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df8ae-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df8ae-107">설명</span><span class="sxs-lookup"><span data-stu-id="df8ae-107">DESCRIPTION</span></span>
<span data-ttu-id="df8ae-108">**Get-AzNetAppFilesActiveDirectory** cmdlet은 ANF 계정 Active Directory 구성에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="df8ae-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="df8ae-109">예제</span><span class="sxs-lookup"><span data-stu-id="df8ae-109">EXAMPLES</span></span>

### <span data-ttu-id="df8ae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="df8ae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="df8ae-111">이 명령은 MyAnfAccount라는 AZURE NETApp Files(ANF) 계정의 MyADConfigName이라는 AD 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df8ae-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="df8ae-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df8ae-112">PARAMETERS</span></span>

### <span data-ttu-id="df8ae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df8ae-113">-AccountName</span></span>
<span data-ttu-id="df8ae-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="df8ae-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8ae-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="df8ae-115">-AccountObject</span></span>
<span data-ttu-id="df8ae-116">새 Active Directory 개체에 대한 계정</span><span class="sxs-lookup"><span data-stu-id="df8ae-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df8ae-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="df8ae-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="df8ae-118">ANF Active Directory의 ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="df8ae-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8ae-119">-DefaultProfile</span></span>
<span data-ttu-id="df8ae-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df8ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df8ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="df8ae-122">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="df8ae-122">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8ae-123">CommonParameters</span></span>
<span data-ttu-id="df8ae-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df8ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8ae-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df8ae-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8ae-126">입력</span><span class="sxs-lookup"><span data-stu-id="df8ae-126">INPUTS</span></span>

### <span data-ttu-id="df8ae-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="df8ae-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="df8ae-128">출력</span><span class="sxs-lookup"><span data-stu-id="df8ae-128">OUTPUTS</span></span>

### <span data-ttu-id="df8ae-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="df8ae-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="df8ae-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df8ae-130">NOTES</span></span>

## <span data-ttu-id="df8ae-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df8ae-131">RELATED LINKS</span></span>
